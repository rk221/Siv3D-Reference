﻿# Siv3D January 2016 リリースノート

- 新機能
 - <b>Visual Studio 2015 対応</b>
 - <b>x64 対応</b>
 - <b>TCP 通信によるネットワーク機能</b>
 - <b>シリアライズ / デシリアライズ</b> (Thanks @Gorei_50)
 - <b>手書き文字 & 図形認識機能</b>
 - <b>再生している動画のフレームを Image や Texture として取得できる機能</b>
 - <b>RenderTexture</b>
 - <b>2D 描画時のカスタム頂点シェーダ</b>
 - <b>Mesh 描画時のカスタム頂点シェーダ・ピクセルシェーダに対応</b>
 - <b>頂点シェーダによる高速な 2D 形状・パーティクル生成</b>
 - <b>直前のフレームを Texture として取得する機能</b>
 - <b>あらゆる 2D 図形を格納できる Shape 型</b>
 - <b>複数台の Web カメラを同時に扱えるように</b>
 - <b>Web カメラの解像度変更に対応</b> (Thanks furafura)
 - <b>複数台のマイクを同時に扱えるように</b>
 - <b>マイク録音のバッファが終端まで達した場合、自動的に先頭に戻る機能を追加</b> (thanks @GRGSIBERIA)
 - <b>2D 描画時のシザー矩形に対応</b>
 - <b>3D 描画時のシザー矩形に対応</b>
 - <b>.exe に埋め込んだファイルのロードに対応</b>
 - <b>2 次ベジェ曲線と 3 次ベジェ曲線を表現するクラスを追加</b>
 - <b>文字列から式を評価する、数式処理機能を追加</b><br>
 - <b>ZIP の書き出しをする ZIPWriter クラスを追加</b>
 - <b>暗号化データが正しく復号できたか検証する機能を追加</b>
 - <b>再生している MIDI サウンドのピッチ変更に対応</b>
 - <b>MIDI ファイルのノート情報の取得に対応</b>
 - <b>スピードが変更可能なストップウォッチクラスを追加</b>
 - <b>マルチスレッドで複数の Image を読み込み・保存する機能を追加</b>
 - <b>マルチスレッドで複数の Wave を読み込み・保存する機能を追加</b>
 - <b>ファイルの変更や削除を検出する FileMonitor クラスを追加</b>
 - <b>ファイルダウンロード、HTTP リクエストを同時に複数扱えるように</b>
 - <b>デスクトップの背景と、画面全体のスクリーンショットを取得する機能を追加</b> (Thanks @hamukun8686)
 - <b>2D 描画の前後関係を Graphics2D::SetZ(uint16) を使い 65536 段階で指定可能に</b>
 - <b>2D 描画時のマルチテクスチャに対応</b>
 - <b>3D 描画時のマルチテクスチャに対応</b>
 - <b>Opus 形式のオーディオファイルの読み込みと書き出しに対応</b>
 - <b>標準 GUI にカラーパレットを追加</b>
 - <b>Forward レンダリング時の最大光源数を 4 に拡充</b>
 - <b>3D 線分を描画する Line3D::drawForward()</b>
 - DynamicTexture が sRGB に対応
 - Rect::Rect() のオーバーロード追加
 - Ray と Plane の交差判定を追加
 - Ray と Disc の交差判定を追加
 - Grid::insert_row(), Grid::erase_row() を追加
 - Grid::swap() を追加
 - DecimalPlace のための _dp User-defined literal を追加
 - PyFmt のための _fmt User-defined literal を追加
 - Hours, Minutes 等の時間の Format に対応
 - CharacterSet::FromUTF32() を追加
 - CharacterSet::ToUTF32() を追加
 - CharacterSet::PercentEncode() を追加
 - Time::GetMillisec64() を追加
 - 単一ファイルのサイズを高速に取得する Filesystem::FileSize() を追加
 - ByteArray::read(), ByteArray::lookahead() のオーバーロードを追加
 - Grid を Initializer lists で初期化できるように
 - AllOf, NoneOf, AnyOf が配列にも対応
 - Stopwatch64 クラスを追加
 - Stopwatch を初期化と同時に start させるオプションを追加
 - BOM なしの UTF-8 テキストをエンコード指定なしでも開けるように
 - BOM なしのテキスト出力に対応
 - initializer-list の Format に対応
 - Deflate によるデータ圧縮機能を追加
 - _pi ユーザ定義リテラルを追加
 - _deg ユーザ定義リテラルを追加
 - 乱数エンジンをスレッドごとに作成するように
 - Ellipse と Line の交差判定に対応
 - Ellipse と Rect の交差判定に対応
 - Ellipse と LineString の交差判定に対応
 - LineString::calculateBoundingRect() を追加
 - Vec2, Vec3, Vec4::setLength(double) を追加
 - VS の出力ウィンドウに Image のサムネイルを出力可能に
 - 相対パスを求める FileSystem::Relative() を追加
 - IReader からの PPM のロードに対応
 - AnimatedGIFWriter クラスを追加
 - Image::clip() のオーバーロードを追加
 - IReader からの Zip のロードに対応
 - Ellipse::writeFrame() / overwriteFrame() を追加
 - MD5 の値を表現する MD5Value 型を追加
 - ファイルやデータの暗号・復号を簡単にする関数を追加
 - Optional に has_value() メンバ関数を追加
 - Time::GetNanosec() を追加
 - Midi::GetPosSec() が返す再生位置を、ノートごとではなくリアルタイムで更新するよう改善
 - MIDI メッセージ作成のためのユーティリティ関数を追加 (Thanks @Pctg_x8)
 - Array&lt;bool&gt; に all(), any(), none() メンバ関数を追加
 - Serial に looahead(), skip() メンバ関数を追加
 - FileSystem::VolumePath() を追加
 - Filesystem::NormalizePath() を追加
 - R16G16, B5G6R5, R32G32B32A32F, R16F, R16G16F, R16G16B16A16F, R32F, R32G32F 形式の DDS 画像を Image として読み込めるように
 - Grid に Point や Size を受け取るオーバーロードを追加
 - Imaging::EdgePreservingFilter() を追加
 - Imaging::DetailEnhance() を追加
 - Imaging::Stylization() を追加
 - ImageR16F, ImageRG16F, ImageRG32F を追加
 - Wave::Wave() のオーバーロードを追加 (Thanks LSMPM)
 - Wave に assign(), insert(), erase(), push_back(), pop_back() メンバ関数を追加 (Thanks LSMPM)
 - 音階を表す enum class PitchName を追加
 - PitchName から周波数を計算する機能を追加
 - Ogg ファイルからループ情報を取得する機能を追加 (Thanks @Pctg_x8)
 - LineString::LineString() のオーバーロードを追加
 - LineString に assign(), insert(), erase() 等のメンバ関数を追加
 - KeyCombination に operator ==, != を追加 (Thanks hanagebatake)
 - Image::getPixel() / sample(), operator[] にオーバーロードを追加
 - Rect, RectF に operator==, != を追加
 - Graphics2D::SetDepthState() / GetDepthState() を追加
 - Texture::operator() のオーバーロードを追加
 - Polygon::draw() に、頂点ごとに異なるカラーを指定するためのオーバーロードを追加 (Thanks yuki)
 - クライアント座標とスクリーン座標を相互に変換する機能を追加 (Thanks @Wp120_3238)
 - Effect::clear() を追加 (Thanks @tyanmahou)
 - RoundRect::center を追加
 - std::hash&lt;Point&gt; の特殊化を追加
 - イージング関数をテンプレート引数にとる EaseIn, EaseOut, EaseInOut を追加 (Thanks @Pctg_x8)
 - Lerp をより柔軟に
 - PerlinNoise に [0, 1] の範囲で結果を返すメンバ関数を追加
 - TextureAsset, SoundAsset をファイルアーカイブから作成する際のユーティリティを追加
 - リモートデスクトップ環境での動作をサポート
 - Vec2 を返すマウス座標関数を追加
 - Color::Color(HSV), ColorF::ColorF(HSV) を追加
 - UV をカスタマイズできる Box の MeshData を追加
- パフォーマンス改善
 - <b>BinaryWriter と TextWriter を 64kB までバッファリングするようにし、頻繁に write() する際のパフォーマンスを改善</b> (Thanks axel)
 - <b>テキストファイルの内容をすべて読み込む際のパフォーマンスを大幅に改善</b>
 - <b>BMP のエンコード / デコードの速度を大幅に改善</b>
 - <b>Random() の速度を改善</b>
 - <b>MIDI 再生時の CPU 使用率を低減</b>
 - <b>Serial::read() のパフォーマンスを改善</b>
 - <b>Web カメラ使用時の CPU 使用率を低減</b>
 - <b>CSVReader, INIReader, JSONReader の hasChanged() を大幅に高速化</b>
 - <b>Ogg Vorbis オーディオのエンコードを高速化</b>
 - <b>AR マーカー検出有効時の CPU 使用率を低減</b>
 - CharacterSet::WidenAscii() の速度を改善
 - CharacterSet::NarrowAscii() の速度を改善
 - Time::UtcOffsetMinutes() の速度を改善
 - MD5 計算の速度を改善
 - TIFF のエンコードの速度を改善
 - GIF のエンコード / デコードの速度を改善
 - Image のモザイク処理の速度を改善
 - 2D 描画シェーダのパフォーマンスを改善
 - 3D 描画のパフォーマンス改善
 - その他各機能のパフォーマンス改善
- バグ修正
 - libqrencode.dll のロードに失敗してアプリが起動しないことがあった問題を修正
 - Grid::inBounds() が正しくなかったバグを修正 (Thanks @siguma323)
 - 不正な頂点配列で Polygon を初期化した際に boundingRect が未初期化の値になっていたバグを修正 (Thanks @reanisz)
 - MultiPolygon の boundingRect とあたり判定が正しくなくなるケースがあったバグを修正 (Thanks dragonicecle)
 - GUIToggleSwitch::setRight()/setLeft()/setIsRight() を実行するとトグルスイッチ自体の有効無効が切り替わってしまったバグを修正 (Thanks @agehama_)
 - Graphics3D::ResetScene() ですべてのライトがリセットされなかったバグを修正 (Thanks 砂時 計)
 - Graphics2D::GetBlandState() / Graphics3D::GetBlandStateForward() のスペルミスを修正 (Thanks 砂時 計)
 - "Resource.hpp" という名前のヘッダをプロジェクトで使うとビルドエラーになる不具合を修正 (Thanks dragonicecle)
 - Optional の仕様を改善
 - Camera の設定が Mouse::Ray() に即座に反映されなかった不具合を修正
 - フォルダに対する FileSystem::Extension(), FileSystem::Basename(), FileSystem::FileName() の結果を修正
 - 長さの無い Line の Line::closest() が NaN を返していた不具合を修正 (Thanks dragonicecle)
 - MultiPolygon が空の Polygon を持つことができた不具合を修正
 - ユーザインデックスが異なり、ボタンが同じ Gamepad や XInput のキーを | を使った KeyCombination でまとめられなかったバグを修正 (Thanks @tyanmahou)
 - EyeXState::clientFixationPos のスペルミスを修正
 - DirectX ランタイムの URL を修正
 - Waving::ChangeTempoAndPitchSemitones() の tempo と pitchSemitones が逆だったバグを修正
 - Wave::MinSamplingRate のスペルミスを修正
 - &lt;Siv3DAddon/LeapMotion.hpp&gt; のバグを修正 (Thanks そつけんぐらし)
 - FileArchive のオープンに失敗したり、存在しないファイルをロードするとクラッシュすることがあったバグを修正 (Thanks gorei50)
 - Graphics2D::BeginShader() が成功にもかかわらず false を返していたバグを修正
 - ウィンドウが非表示の時にダイアログが出現しないことがあった不具合を修正
 - DPI 設定に起因した TobiiEyeX の座標ずれの問題を修正 (Thanks @tyanmahou)
 - 大量にファイルをドロップした際に取得漏れや例外が生じることがあった問題を修正 (Thanks furafura)
 - Mouse::Transorm() と図形のあたり判定に関連するバグを修正 (Thanks @hamukun8686)
 - 一部の Intel の iGPU で Particle の色が正しくなくなることがあった問題を修正 (Thanks @hisoji)
 - その他細かなバグ修正
- 仕様変更
 - <b>Timer 系クラスを Stopwatch に名称変更</b> (Thanks @Rinifisu)
 - <b>DynamicSound の機能を Sound に統合</b>
 - <b>TimerMillisec, TimerSec, TimerMinute を Stopwatch に統合、古いクラスは legacy 名前空間へ移動</b>
 - <b>EventTimer は新しい Stopwatch クラスを使用するよう仕様変更、古いクラスは legacy 名前空間へ移動</b>
 - <b>TextReader::path や Point::isZero など、多くのプロパティをメンバ関数に変更</b>
 - <b>Internet 名前空間のファイルダウンロード・HTTP リクエスト系関数を廃止、HTTPClient クラスに移行</b>
 - <b>Webcam 名前空間の機能を Webcam クラスに移行</b>
 - <b>Webcam 名前空間の一部の関数を WebcamManager 名前空間に移動</b>
 - <b>Reocrder 名前空間の機能を Reocrder クラスに移行</b>
 - <b>Reocrder 名前空間の一部の関数を ReocrderManager 名前空間に移動</b>
 - <b>Plane は両面表示するよう仕様変更</b>
 - <b>Disc は両面表示するよう仕様変更</b>
 - <b>Stopwatch の戻り値の型を符号なし整数型から符号付き整数型に変更</b>
 - <b>TextReader::readContents() を廃止、仕様を変更して TextReader::readAll() に移行</b>
 - <b>MemoryReader を ByteArray に名称変更</b>
 - <b>ファイル圧縮アーカイブを作る Compression 系関数を廃止、Compression::Compress() / Decompress() と ZIPWriter に移行</b>
 - <b>Logger::WriteImage() を廃止、LOG() と統合</b>
 - <b>Imaging::SaveAnimatedGIF() を廃止、AnimatedGIFWriter に移行</b>
 - <b>Crypto::～ 系関数を廃止、仕様を改善した Crypto2::～ に移行</b>
 - <b>Serial::readByte(), readBytes() を read() に統合</b>
 - <b>Quaternion のデフォルトコンストラクタは単位クォータニオンで初期化するよう仕様変更</b> (Thanks @Wp120_3238)
 - <b>Graphics2D::BeginShader() は Graphics2D::BeginVS() と Graphics2D::BeginPS() に移行</b>
 - <b>Graphics2D::EndShader() は Graphics2D::EndVS() と Graphics2D::EndPS() に移行</b>
 - <b>Mouse::LeftClicked(), RightClicked() を廃止</b>
 - <b>クライアント領域外の図形の部分については leftClicked, rightClicked が適用されないよう仕様変更</b> (Thanks @hamukun8686)
 - <b>Input::MouseL 等は、クライアント領域外ではクリック判定しないよう仕様変更</b> (Thanks @hamukun8686)
 - <b>ファイルアーカイブの際、アーカイブされた各ファイルの名前が元のディレクトリ名を含むよう仕様変更</b>
 - <b>AR の機能を Webcam クラスに統合</b>
 - <b>仮想フルスクリーンを標準のフルスクリーンに</b>
 - ウィジェットの作成関数は IWidget でなくウィジェット自身のポインタを返すよう仕様変更 (Thanks sigureya)
 - 一部の Ray::test() を Ray::intersectsAt() に移行
 - MemoryReader::asArray() は参照を返すよう仕様変更
 - Grid::push_row() を Grid::push_back_row() に名称変更
 - Grid::pop_row() を Grid::pop_back_row() に名称変更
 - Char クラスを廃止
 - EventTimer::setEvent() を addEvent() に名称変更
 - 不具合のため CopyOption::Confirm_if_exists を一時的に廃止 (Thanks しぐれん)
 - 空の Format() を可能に
 - MemoryWriter::toMemoryReader() を MemoryWriter::toByteArray() に名称変更
 - XMLReader のメンバ関数を修正
 - Color::code を廃止
 - Color/ColorF の grayscale プロパティをメンバ関数に変更 
 - LineString::operator[] を LineString::point() に名称変更
 - ZipReader を ZIPReader に名称変更
 - MD5 関数の戻り値を String から MD5Value に変更
 - Serial クラスのメンバ関数の名前と仕様を変更
 - VideoReader::length を num_frames に名称変更
 - VideoReader::read() を readFrame() に名称変更
 - VideoWriter::write() を VideoWriter::writeFrame() に名称変更
 - QR::Encode() のスペルミスを修正
 - スプラッシュウィンドウをなめらかにフェードインさせて表示するよう仕様変更
 - Grid::size() を Grid::num_elements() に名称変更、Grid::size() は Size を返すよう仕様変更
 - RecorderFormat を RecordingFormat に名称変更
 - Waving::Synthesize() を廃止、Wave::Wave() に機能を移動
 - Effect::isActive を廃止、Effect::isPaused() を使うように
 - Graphics2D::SetUVTransform(), GetUVTransform() を廃止、必要な場合はカスタム頂点シェーダを利用するように
 - FileArchive のファイル名は、小文字と大文字を区別しないように
 - RasterizerState の定数の名称を変更
 - その他細かな仕様変更
- その他
 - 付属の M+ フォントを更新。対応漢字が 4,900 から 5,000 に
 - libpng のバージョンを 1.6.16 から 1.6.18 に更新
 - libjpeg-turbo のバージョンを 1.3.1 から 1.4.2 に更新
 - OpenJPEG のバージョンを 1.5.0 から 1.5.2 に更新
 - OpenCV のバージョンを 2.4.9 から 3.0.0 に更新
 - 内部で使用する Boost のバージョンを 1.57.0 から 1.59.0 に更新
 - libmpg123 のバージョンを 1.20.1 から 1.22.0 に更新
 - libogg のバージョンを 1.3.0 から 1.3.2 に更新
 - libvorbis のバージョンを 1.3.3 から 1.3.5 に更新
 - SoundTouch library のバージョンを 1.8.0 から 1.9.2 に更新

