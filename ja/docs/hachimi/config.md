# 設定

このページでは、設定オプションの一覧と、その使用目的について説明します。

設定ファイルは以下の場所にあります。

- Windows: `[ゲームのインストールフォルダ]\hachimi\config.json`
- Android: `/sdcard/Android/media/jp.co.cygames.umamusume/hachimi/config.json`

::: warning
このファイルを通常のテキストエディタで編集すると、ファイルが破損する可能性があります。Androidの場合は「Acode」または「QuickEdit」などを、Windows の場合は「Notepad++」などの適切なテキストエディタを使用してください。
:::

**注:** これらのオプションの一部は設定エディタ機能では使用できないため、手動で追加する必要があります。

- `debug_mode`: デバッグモードを有効にします。現在はデバッグログの有効化、無効化のみを行います。
- `translator_mode`: 翻訳者向けのオプションを有効にします。翻訳されていない UI の文字列をコンソールに記録し、翻訳者にとって便利な他の機能を有効にします。
- `disable_gui`: 内蔵 GUI を無効にします。これにより翻訳データのアップデート機能も無効になるのでご注意ください。
- `localized_data_dir`: ローカライズされたデータのディレクトリを設定します。ローカライズされたデータの設定ファイルが必要です。
- `target_fps`: ゲームのターゲット FPS を設定します。設定されていない場合、Hachimi はゲームの FPS を変更しようとしません。`vsync_count` が設定されている場合は反映されません。
- `open_browser_url`: GUI からゲーム内ブラウザを起動したときに開く際のデフォルトの URL を設定します。デフォルトの値： `https://www.google.com/`
- `virtual_res_mult`: 仮想解像度の倍率を設定します。デバイスの性能が十分な場合は、1.5 または 2 が適切な値です。それ以上の値はおそらく過剰です。「ソフトリスタート」を行うことで、ゲームを終了せずに適用できます。
- `gui_scale`: 内蔵GUIのサイズを変更します。デフォルトの値：`1.0`
- `render_scale`: レンダリング解像度スケールの倍率を設定します。値が大きいほど鮮明になりますが、ゲームのパフォーマンスは低下します。デフォルトの値：`1.0`
- `msaa`: ゲームのレンダリング時の MSAA（アンチエイリアシング）のレベルを調整します。高い値に設定すると、輪郭が滑らかになりますが、パフォーマンスが低下する可能性があります。
- `aniso_level`: テクスチャの異方性フィルタリングのレベルを調整します。GPU の使用率が高くなりますが、テクスチャがくっきり見えるようになります。
- `translation_repo_index`: 翻訳レポジトリのインデックスURLを設定します。翻訳データのアップデート機能によって使用されます
- `skip_first_time_setup`: 起動時に初回セットアップをスキップするかどうかを設定します。初回セットアップを閉じると自動的に `true` に設定されます。
- `disable_auto_update_check`: 起動時の自動アップデート確認機能を無効にします。
- `disable_translations`: 翻訳を無効にします。
- `disable_skill_name_translation`: 他の部分の翻訳を有効にしたまま、スキル名の翻訳のみを無効にします。
- `meta_index_url`: 利用可能なリポジトリを取得するために使用されるメタインデックス URL を設定します。
- `ui_scale`: UIサイズの倍率を設定します。デフォルトの値：`1.0` （変更なし）
- `hide_ingame_ui_hotkey`: ゲームの UI を非表示にする内部ホットキーを有効にします。Android でこれを有効にした場合、`画面右上を3回タップ`することでも同様に動作します。
- `graphics_quality`: グラフィックのクオリティを設定します。設定可能な値： `Default`、`Toon1280`、`Toon1280x2`、`Toon1280x4`、`ToonFull`、`Max`
- `story_choice_auto_select_delay`: ストーリー閲覧時に AUTO を使用している際の、選択肢を選択するまでの遅延（秒）を設定します。デフォルトの値: `0.75`（秒）
- `story_tcps_multiplier`: ストーリー閲覧時のテキストのスピードの倍数（"typewriting count per second"）を設定します。 デフォルトの値： `1.0`
- `enable_ipc`: HTTP プロセス間通信サーバーを有効にし、他のプログラムからゲームを制御できるようにします。翻訳ツールでの使用を目的としています。
- `ipc_listen_all`: ネットワーク上のあらゆるデバイスからの IPC コマンドを受け入れます。**必要がない場合はこのオプションを有効にしないでください。**
- `force_allow_dynamic_camera`: あらゆるタイプのレースでダイナミックカメラを選択できるようにします。
- `live_theater_allow_same_chara`: ライブシアターの編成で同じキャラクターを複数回選択できるようにします。また、編成の自動保存を無効にします。**この機能を使用して作成したキャラクターの編成を手動で保存しないでください。**
- `physics_update_mode`: 物理演算のモードを変更します。設定可能な値：`ModeNormal`、`Mode60FPS`、`SkipFrame`、`SkipFramePostAlways`
- `ui_animation_scale`: UI のアニメーション速度の倍率を設定します。デフォルトの値：`1.0`
- `sugoi_url`: Sugoi Offline Translator または自動翻訳対応の翻訳サーバーの URL を設定します。通常の Sugoi Offline Translator の設定の場合は、このオプションを設定する必要はありません。デフォルトの値： `http://127.0.0.1:14366`
- `auto_translate_stories`: 自動翻訳機能を使用してストーリーを翻訳します。
- `auto_translate_localize`: 自動翻訳機能を使用して UI テキストを翻訳できます。ただし、ほとんどの自動翻訳エンジンは改行や書式設定タグを適切に維持できないため、通常このオプションの使用は推奨されません。
- `disabled_hooks`: フックを手動で無効にします。このオプションは互換性の問題を解決するためのデバッグツールであるため、必要がない場合はこのオプションを変更しないでください。
- `enable_file_logging`: ログを `hachimi.log` としてゲームのディレクトリに保存します。このオプションが無効になっている場合や、ファイルを作成できなかった場合は、デバッグ用のアウトプットのみに出力されます。デフォルトの値：`false`
- `lazy_translation_updates`: レポジトリで変更されていない翻訳ファイルのダウンロードをスキップします。アップデートが速くなりますが、端末のファイルが古い場合や破損している場合でもそのファイルのダウンロードは行ないません。デフォルトの値：`false`
- `shadow_resolution`: 影のクオリティを調整します。高い値に設定すると、影のディテールは向上しますが、パフォーマンスが低下する可能性があります。
- `skill_info_dialog`: ゲーム内でスキルを表示する際に、スキルに関する詳細情報を表示します。

## Windows のみ

- `vsync_count`: VSync カウントを設定します。1 に設定すると、ゲームの FPS がモニターのリフレッシュレートに同期されます。詳しくは[こちら（Unity docs）](https://docs.unity3d.com/ScriptReference/QualitySettings-vSyncCount.html)
- `load_libraries`: 起動時に読み込むライブラリのリストを設定します。他のMODの読み込みにも使用できます。 例： `["applejuicer.dll", "banana.dll"]`
- `menu_open_key`: メニューを開くキーの Windows VK コードを設定します。デフォルトの値は： `39` （右矢印キー）です。すべてのキーコードの一覧は[こちらページ](https://cherrytree.at/misc/vk.htm)でご確認ください。
- `auto_full_screen`: ゲームの向きが画面の向きと一致すると、ゲームを自動的にフルスクリーンモードにします。現時点では、Hachimi は他のアスペクト比をサポートしておらず、フルスクリーン解像度は常に 16:9 にスケーリングされます。このオプションを使用する場合は、`full_screen_mode` と `resolution_scaling` を適切な値に設定してください。
- `full_screen_mode`: 使用するフルスクリーンモードを設定します。使用可能な値は：`ExclusiveFullScreen`、`FullScreenWindow`（ボーダーレスフルスクリーン）です。画面のアスペクト比が16:9でない場合は、`ExclusiveFullScreen`を使用してください。ゲーム画面が適切にスケーリングされません。
- `resolution_scaling`: 解像度のスケーリングモードを設定します。使用可能な値は：`Default`、`ScaleToScreenSize`、`ScaleToWindowSize`です。1080p を超える解像度の画面で `auto_full_screen` を使用する場合は、`ScaleToScreenSize`（推奨）または `ScaleToWindowSize` を使用してください。ゲーム画面が適切にスケーリングされません。
- `block_minimize_in_full_screen`: フルスクリーンでの最小化をブロックします。`FullScreenWindow` に設定している場合のみ使用してください。
- `window_always_on_top`: ゲームウィンドウを常に他のウィンドウより手前に表示します。
- `disable_gui_once`: 内蔵 GUI を次回の起動時のみ無効にします。次回の起動時に自動的に `false` にリセットされ、強制的に `disable_gui: true` を設定します。これによって Steamストア での購入が可能になります。
- `discord_rpc`: Discord の RPC（Rich Presence Integration）を DMM 等の RPC がサポートされていないプラットフォームで有効化します。これにより、Discord のプロフィールにウマ娘のアクティビティが表示されます。
