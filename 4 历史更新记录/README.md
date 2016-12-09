## 历史更新记录

* 1.4.0 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.4.0.md))
  - 发布 pldroid-player-1.4.0.jar
  - 更新 libpldroidplayer.so
  - 新增设置封面功能
  - 新增获取当前播放状态接口
  - 修复了多次打开、关闭播放器出现 ANR 的问题
  - 修复了播放地址含有多个 domain 时解析异常的问题

* 1.3.2 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.3.2.md))
  - 发布 pldroid-player-1.3.2.jar
  - 修复了部分场景下直接使用 PLMediaPlayer 播放出现的崩溃问题

* 1.3.1 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.3.1.md))
  - 发布 pldroid-player-1.3.1.jar
  - 更新 libpldroidplayer.so
  - 添加了 QoS 功能
  - 优化了纯音频播放的累积延时
  - 修复了在部分场景下频繁重连导致的崩溃问题
  - 修复了 DNS 解析优化在某些机型上出现崩溃的问题
  - 修复了当服务端主动断开 TCP 连接，客户端没重连的问题
  - 修复了 x86_64 架构下找不到动态库导致的崩溃问题
  - 更新了 demo 代码，演示了如何进行重连

* 1.3.0 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.3.0.md))
  - 发布 pldroid-player-1.3.0.jar
  - 更新 libpldroidplayer.so
  - 优化直播累积延时
  - 优化首开时间
  - 优化播放器退出耗时较长
  - 支持带 IP 地址的播放 URL
  - 新增 PLNetworkManager 类，提供 DNS 缓存管理服务
  - 新增 AVOptions 累积延时相关的配置参数
  - 新增多种新的回调信息，方便更准确地感知播放过程中的状态变化
  - 修复动态构建 PLVideoTextureView 导致崩溃的问题
  - 修复 onError 回调 extra 为 0 的情况
  - 修复了部分码流的时长解析不准确的问题
  - 修复点播缓冲过程中，断网操作导致长时间无法恢复的问题
  - 修复特殊网络情况下，退出播放器时的 ANR 问题

* 1.2.3 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.2.3.md))
  - 发布 pldroid-player-1.2.3.jar
  - 更新 libpldroidplayer.so
  - 支持后台播放
  - 优化点播的首开时间
  - 优化直播过程中的累积延时
  - 新增 `setWakeMode` 和 `setScreenOnWhilePlaying` 接口
  - 新增 `setLooping` 和 `isLooping` 接口
  - `AVOption` 添加 `prepare timeout` 超时的配置
  - 修改 `seekTo` 的参数，类型改为`long` 型
  - 解决播放部分纯音频流的时候，获取不到时长的问题
  - 解决从后台切换回来后，播放从头开始加载的问题
  - 修复`AudioManager`可能导致的内存泄漏问题

* 1.2.2 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.2.2.md))
  - 发布 pldroid-player-1.2.2.jar
  - `AVOptions` 新增 `KEY_START_ON_PREPARED` 参数，便于配置是否自动开始播放
  - `PLVideoTextureView` 新增 `setMirror` 接口，可实现画面镜像变换
  - 新增 `setVolume` 接口，可实现播放器音量的设置，或静音功能

* 1.2.1 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.2.1.md))
  - 发布 pldroid-player-1.2.1.jar
  - 恢复 `SharedLibraryNameHelper.renameSharedLibrary` 接口
  - 恢复 `SharedLibraryNameHelper.getSharedLibraryName` 接口

* 1.2.0 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.2.0.md))
  - 发布 pldroid-player-1.2.0.jar
  - 删除了 ijkmediaplayer.jar
  - 实现播放器秒开优化，网络条件好的情况下，可以实现秒开
  - 新增播放器核心类 `PLMediaPlayer`
  - 新增` PLVideoView` 控件
  - 新增`PLVideoTextureView` 控件
  - 支持多种画面预览模式，包括：原始尺寸、适应屏幕、全屏铺满、16:9、4:3 等
  - 支持画面旋转（0度，90度，180度，270度）
  - 更新 Demo 程序，演示所有新增的接口类

* 1.1.4 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.1.6.md))
  - 发布 pldroid-player-1.1.4.jar
  - 更新 libpldroidplayer.so
  - 新增播放器全屏播放支持
  - 新增纯音频播放 `AVOptions` 支持
  - 修复播放过程中，概率性异常地回调 `onCompletion` 问题
  - `VideoView` 布局的展示代码

* 1.1.3 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.1.4.md))
  - 发布 pldroid-player-1.1.3.jar
  - 更新 libpldroidplayer.so
  - 新增 ARM, X86 支持
  - 新增 `KEY_LIVE_STREAMING` option
  - 修复 `getCurrentPosition` 和 `getDuration` 返回值异常问题
  - 修复播放过程中，概率性不间断地回调 onCompletion 问题
  - 更新不同播放方式（直播或点播）设置 option 的展示代码

* 1.1.2 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.1.3.md))
  - 发布 pldroid-player-1.1.2.jar
  - 更新 arm64-v8a/libpldroidplayer.so，armeabi-v7a/libpldroidplayer.so
  - 修复推流端断流后，Player 概率性地无 `onCompletion` 回调通知
  - 修复 `AVOptions` 的 key 没有设置 value 时候的 Crash 问题

* 1.1.1 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.1.2.md))
  - 发布 pldroid-player-1.1.1.jar
  - 发布 arm64-v8a/libpldroidplayer.so，增加 ARM64v8a 支持
  - 更新 ARMv7a 版本的 libpldroidplayer.so
  - 增加 `AVOptions` 类，可设置如下属性：
    * `AVOptions.KEY_GET_AV_FRAME_TIMEOUT`  // ms
    * `AVOptions.KEY_MEDIACODEC`            // 1 means enable, 0 means disable
    * `AVOptions.KEY_FFLAGS`                // "nobuffer"
    * `AVOptions.KEY_BUFFER_TIME`           // ms
  - 修复部分音视频流无法播放的问题
  - 修复仅含视频流无法播放的问题
  - 优化连接时间
  - 废除 `setBufferTime(float ms)` 接口，使用 `AVOptions` 代替
  - 增加 `AVOptions` 的演示代码

* 1.1.0 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.1.1.md))
  - 发布 pldroid-player-1.1.0.jar
  - 更新 ijkmediaplayer.jar
  - 更新 libpldroidplayer.so
  - 添加纯音频播放接口，支持后台运行
  - 添加 bufferTime 设置接口：`setBufferTime(float ms)`
  - 添加状态码：`EXTRA_CODE_CONNECTION_REFUSED` 和 `EXTRA_CODE_EOF`
  - 优化播放延时
  - 优化播放过程中因断流导致的等待时间
  - 修复部分机型硬解码异常问题
  - 添加纯音频播放展示界面

* 1.0.0 ([Release Notes](https://github.com/pili-engineering/PLDroidPlayer/blob/master/ReleaseNotes/release-notes-1.1.0.md))
  - 发布 PLDroidPlayer v1.0.0

