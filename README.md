# Rime

My Rime configuration.


## Snapshot

Linux Snapshot:

![Linux Snapshot](https://raw.githubusercontent.com/alswl/Rime/master/snapshots/linux-rime.png)

macOS Snapshot:

apathy scheme:

![Mac apathy theme Snapshot](https://raw.githubusercontent.com/alswl/Rime/master/snapshots/mac-rime-apathy.png)

homepage scheme:

![Mac homepage theme Snapshot](https://raw.githubusercontent.com/alswl/Rime/master/snapshots/mac-rime-homepage.png)

Emoji Snapshot:

![Emoji Snapshot 1](https://raw.githubusercontent.com/alswl/Rime/master/snapshots/emoji-1.png)

![Emoji Snapshot 2](https://raw.githubusercontent.com/alswl/Rime/master/snapshots/emoji-2.png)

Kaomoji Snapshot:

![Kaomoji Snapshot](https://raw.githubusercontent.com/alswl/Rime/master/snapshots/kaomoji.png)

Poetry Snapshot:

![Poetry Snapshot](https://raw.githubusercontent.com/alswl/Rime/master/snapshots/poetry.png)


## Feature

*   double Pingyin input
*   official website UI
*   Apple offical input method UI
*   include Chinese Pinyin to Emoji mapping


## Requirements

*   Linux
    *   librime>=1.3
    *   opencc>=1.0.2
*   macOS
    *   test in 0.9.27
    *   DO NOT install 0.9.20, it is a old deprecated version. You should build from source.


## Structure

*   User defined files
    *   `default.custom.yaml`：自定义配置
    *   `squirrel.custom.yaml`: macOS Squirrel 鼠须管自定义配置
    *   `luna_pinyin.custom.yaml`：明月拼音自定义配置（模糊音在此）
    *   `double_pinyin.custom.yaml`：双拼自定义配置
    *   `luna_pinyin.custom.dict.yaml.sample`：拼音自定义字典（使用 `import_tables`
        引入其他 dict），使用时需要**重命名**为 `luna_pinyin.custom.dict.yaml`
*   Dictionary
    *   `luna_pinyin.dict.yaml`：明月拼音（Rime 自带）
    *   `luna_pinyin.extended.dict.yaml`：明月拼音擴充詞庫（Rime 自带）
    *   `luna_pinyin.hanyu.dict.yaml`：汉语大词典（Rime 自带）
    *   `luna_pinyin.chengyusuyu.dict.yaml` 成语俗语（搜狗）
    *   `luna_pinyin.sijixingzhenquhuadimingciku.dict.yaml`: 四级行政区划地名词库（搜狗）
    *   `luna_pinyin.jisuanjicihuidaquan.dict.yaml`：计算机词汇大全（搜狗）
    *   `luna_pinyin.wangluoliuxingxinci.dict.yaml`: 网络流行新词（搜狗）
    *   `luna_pinyin.shanghaishichengshixinxijingxuan.dict.yaml` 上海市城市信息精选（搜狗）
    *   `luna_pinyin.poetry.dict.yaml`：明月拼音擴充詞庫（詩詞）（Rime 自带）
    *   `luna_pinyin.emoji.dict.yaml`：Rime 自带 emoji（Rime 自带）
    *   `luna_pinyin.emoji.apple.dict.yaml`：Apple iOS 10 Emoji
    *   `luna_pinyin.emoji.scomper.dict.yaml`：Scomper 维护 Emoji（包含 Unicode 9.0）
    *   `luna_pinyin.kaomoji.dict.yaml`：搜狗颜文字
*   Generated fiels
    *   `build` folder in Linux, macOS in rime root folder:
        *   `default.yaml`
        *   `squirrel.yaml`
        *   `*.prism.bin`
        *   `*.reverse.bin`
        *   `*.table.bin`
        *   `*.custom.reverse.bin`
    *   `$ROOT` folder:
        *   `*.schema.yaml`
        *   `user.yaml`
    *   Files generated after installation:
        *   `symbols.yaml`
        *   `installation.yaml`

See [rime/plum: 東風破 /plum/: Rime configuration manager and input schema repository](https://github.com/rime/plum)
to gernerate input methods. In short:

```
./plum/rime-install double-pinyin
./plum/rime-install combo-pinyin
```

All `dict.yaml` file can use separately.

Use [alswl/ascel: Another scel parser](https://github.com/alswl/ascel) to convert Sogou scel files.

Author: @alswl .
