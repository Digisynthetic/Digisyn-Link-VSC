# AES67 VSC 虚拟声卡说明书

![VSC LOGO](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/01-vsc_logo_zh.png)

AES67 VSC 虚拟声卡适用于 Windows 环境，可用于发送和接收 AES67 网络音频流。它可以让 Windows 电脑像一台 AES67 音频设备一样接入网络音频系统。

AES67 是一种用于在局域网中传输专业音频的通用协议。音频流的发现、路由和管理需配合 **AES67LINK GUI 控制软件** 使用。AES67LINK GUI 用于发现网络中的 AES67 设备，并在发送通道和接收通道之间建立音频路由。

AES67 VSC 已在多种主流网络音频环境中完成测试，包括 **RAVENNA**、**Dante**、**Q-LAN**、**Telos** 和 **Crestron**。

## 产品特点

- 支持 **48 kHz、96 kHz、192 kHz** 采样率。
- 支持最高 **64 x 64** 通道。
- 支持 Windows **WDM / ASIO** 音频接口。

## 适用范围

本文适用于 Windows 版 AES67 VSC 的下载、安装、激活、功能设置、AES67 音频流管理以及常见问题排查。阅读本文时，可以把 VSC 理解为“安装在电脑里的网络音频设备”，把 AES67LINK GUI 理解为“用于连接各个网络音频设备的软件”。

## 1. 兼容系统版本

- 使用 WDM 音频接口时，系统需为 **Windows 10 22H2** 或更高版本。
- 使用 ASIO 音频接口时，系统需要为 **Windows 10** 或更高版本。

## 2. 下载与安装虚拟声卡

### 2.1 下载虚拟声卡

访问 [https://docs.digisynthetic.com/](https://docs.digisynthetic.com/)，按照下图所示路径下载 VSC 虚拟声卡的 Windows 安装包。下载完成后，应得到一个可在 Windows 上运行的安装程序。

![vsc_windows_download_path](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/03-vsc_windows_download_path_zh.png)

### 2.2 安装虚拟声卡

1. 双击安装包，选择安装语言。安装程序支持简体中文和 English。

![installer_language_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/04-installer_language_selection_zh.png)

2. 根据需要选择是否创建桌面快捷方式和快速运行栏快捷方式，然后点击 “下一步”。

![installer_shortcut_options](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/05-installer_shortcut_options_zh.png)

3. 点击 “安装”，等待安装程序完成。安装完成后，电脑中会安装 VSC 软件和对应的虚拟声卡驱动。

![installer_ready_to_install](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/06-installer_ready_to_install_zh.png)

**<font color="red">注意</font>**： 如果系统启用了 Windows 防火墙，需要允许 `C:\Program Files (x86)\VSC\VSC.exe` 和 `C:\Program Files (x86)\VSC\myAudioRoute.exe` 联网。否则软件可能无法激活，或无法在网络中发现和连接 AES67 设备。

## 3. 语言切换

在软件左下角点击 “中 / En” 按钮，可在简体中文和 English 之间切换界面语言。

![software_language_switch](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/07-software_language_switch_zh.png)

## 4. 激活虚拟声卡

安装完成后，VSC 虚拟声卡需要激活后才能使用。软件支持在线激活和离线激活两种方式。

### 4.1 在线激活虚拟声卡（需要联网）

在线激活适用于可以访问互联网的设备。该方式最简单，软件会通过网络直接验证激活码。

#### 4.1.1 申请在线激活码

在浏览器中访问 [https://docs.digisynthetic.com/](https://docs.digisynthetic.com/) 并注册官方 DOCS 账号。注册成功后，可在页面左下角申请 VSC 在线激活码。

![docs_apply_online_activation_code](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/08-docs_apply_online_activation_code_zh.png)

#### 4.1.2 输入激活码

申请在线激活码后，回到 VSC 软件的激活页面，按以下步骤完成激活：

1. 填入申请到的在线激活码。
2. 点击 “激活” 按钮。

激活成功后，软件即可进入可用状态，之后可以继续设置网卡、采样率、通道数量和音频接口。

![vsc_online_activation](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/09-vsc_online_activation_zh.png)

### 4.2 离线激活虚拟声卡（无需联网）

离线激活适用于无法访问互联网的设备。该方式需要先导出本机机器 ID，由厂家根据机器 ID 生成只适用于这台电脑的激活文件。

#### 4.2.1 申请离线激活文件

复制软件中显示的 “机器 ID”，并将机器 ID 提供给厂家，用于生成对应的离线激活文件。机器 ID 用于识别当前电脑，不同电脑的机器 ID 不同。

![offline_activation_machine_id](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/10-offline_activation_machine_id_zh.png)

#### 4.2.2 导入离线激活文件

从厂家获取激活文件后，回到 VSC 软件的激活页面，按以下步骤完成激活：

1. 选择导入证书激活。
2. 选择厂家提供的 `xxx_license.dat` 文件。
3. 点击右下角的 “打开”，完成本机离线激活。

离线激活成功后，该电脑即可在无网络环境下使用 VSC 虚拟声卡。

![select_offline_license_file](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/11-select_offline_license_file_zh.png)

## 5. 主要功能设置

VSC 的主要功能设置包括网卡、采样率、通道数量、音频接口和启动状态。这些参数决定 VSC 使用哪张网卡传输音频、使用多少个音频通道，以及电脑软件通过哪种音频接口调用 VSC。

修改关键参数后，建议重新开启虚拟声卡，使配置完整生效。

![main_function_settings](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/12-main_function_settings_zh.png)

### 5.1 网卡选择

VSC 需要绑定实际用于 AES67 网络音频传输的有线网卡。绑定网卡后，VSC 会通过这张网卡发送和接收 AES67 音频流。

- 仅支持有线实体网卡。
- 不支持虚拟网卡或无线网卡。
- 如果电脑有多张实体网卡，可展开下拉框选择需要使用的网卡。

![network_adapter_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/13-network_adapter_selection_zh.png)

所选网卡的 IPv4 地址会显示在下方的 “IP 地址” 区域。

![network_adapter_ip_address](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/14-network_adapter_ip_address_zh.png)

**<font color="red">注意</font>**： 无线网络容易受到信号强度、干扰和带宽波动影响，可能导致音频中断、延迟升高或出现杂音。因此不建议使用无线网卡传输 AES67 音频流。

### 5.2 采样率选择

VSC 支持在 **48 kHz、96 kHz、192 kHz** 之间选择采样率。采样率可以理解为音频每秒采集和处理的次数。采样率越高，音频数据量越大，对电脑和网络的要求也越高。

![sample_rate_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/15-sample_rate_selection_zh.png)

**<font color="red">注意</font>**： 与其他 AES67 或 Dante 设备互通时，相关设备的采样率需要保持一致。采样率不一致时，可能无法建立路由，或建立后没有声音。

### 5.3 通道数量选择

可根据授权范围设置 VSC 虚拟声卡的输入和输出通道数量。通道数量决定电脑最多可以同时发送或接收多少路音频信号。

- 在 [https://docs.digisynthetic.com/](https://docs.digisynthetic.com/) 申请的在线激活码默认为 8 通道授权，即输入和输出通道数均为 8。
- 如需更多通道，请联系厂家获取对应授权。

![channel_count_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/16-channel_count_selection_zh.png)

**<font color="red">注意</font>**： 通道数量越多，同时处理的音频数据越多，对 Windows 电脑性能的要求也越高。如果电脑性能不足，可能出现音频卡顿或杂音。

### 5.4 音频接口选择

VSC 支持 **WDM** 和 **ASIO** 两种音频接口。音频接口决定电脑中的软件通过什么方式使用 VSC。

1. **WDM**：在 Windows 系统声音设备中可见，适合普通播放、录音和系统声音场景，例如 Wasapi、WaveOut、DirectSound 等。
2. **ASIO**：通常不在 Windows 系统声音设备中显示，适合专业音频软件直接调用，例如 Reaper、Adobe Audition 等。

ASIO 选项后的时间表示缓冲区大小，也就是音频延迟。数值越小，声音延迟越低；但电脑需要更快处理音频数据，稳定性要求也更高。

![audio_interface_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/17-audio_interface_selection_zh.png)

**<font color="red">注意</font>**： 使用低延迟 ASIO 播放时，如果出现杂音、爆音或声音中断，请适当调高 ASIO 延迟。调高延迟会增加一点声音延迟，但通常可以提升播放稳定性。

### 5.5 开启虚拟声卡

完成参数设置后，需要开启虚拟声卡通道，才能正常使用 VSC 功能。开启后，VSC 才会作为网络音频设备开始工作，并能被 AES67LINK GUI 发现。

- 选择 WDM 音频接口时，需要等待所有系统声道初始化完成后再使用。
- 选择 ASIO 音频接口时，通常可以直接使用。

![start_virtual_soundcard](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/18-start_virtual_soundcard_zh.png)

### 5.6 使用 VSC 作为输入和输出设备

在 Windows “系统设置” → “音量” → “音量合成器” 中，可将 VSC 选择为输入设备（录制）或输出设备（播放）。例如，选择 VSC 作为输出设备后，电脑中的播放声音可以进入 VSC，再通过 AES67 路由发送到网络中的其他音频设备。

![windows_sound_output_input_device](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/19-windows_sound_output_input_device_zh.png)

## 6. 其他设置

本页包含 VSC 的附加参数设置。这些设置通常不需要频繁修改，只有在网络音频系统有特定要求时才需要调整。

**<font color="red">注意</font>**： 本页面中的设置修改后，需要点击 “保存” 才能生效。

![other_settings_save_button](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/20-other_settings_save_button_zh.png)

### 6.1 设置 PTP Domain 时钟域

可在此处设置 AES67 VSC 虚拟声卡所在的 PTP Domain。PTP 用于让网络音频设备使用同一个时间基准，避免不同设备之间播放速度或时间不同步。

PTP Domain 可以理解为一个“时钟同步分组”。只有处于同一 PTP Domain 的设备，才会互相进行时钟同步。

- 如果虚拟声卡已经启动，修改 PTP Domain 后需要重新开启虚拟声卡。
- 重新开启虚拟声卡的方法见 “5.5 开启虚拟声卡”。

![ptp_domain_setting](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/21-ptp_domain_setting_zh.png)

**<font color="red">注意</font>**： 由于 Windows 的时钟精度限制，VSC 虚拟声卡只能跟随其他主时钟设备，不能作为整个 AES67 系统的主时钟。

## 7. 发现与使用虚拟声卡

AES67 VSC 的实际音频流管理需搭配 AES67LINK GUI 控制软件完成。AES67 VSC 负责把电脑变成 AES67 音频设备，AES67LINK GUI 负责在 AES67 VSC 和其他 AES67 设备之间建立音频连接。

AES67LINK GUI 控制软件可从 [https://docs.digisynthetic.com/](https://docs.digisynthetic.com/) 下载。

![aes67link_download_path](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/22-aes67link_download_path_zh.png)

### 7.1 在 AES67LINK GUI 中发现 VSC

无论 VSC 使用 WDM 还是 ASIO 音频接口，开启虚拟声卡后，均可在 AES67LINK GUI 中发现并控制该设备。发现成功后，VSC 会像其他网络音频设备一样显示在 AES67LINK GUI 的设备列表或路由界面中。

![aes67link_discover_vsc_device](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/23-aes67link_discover_vsc_device_zh.png)

**<font color="red">注意</font>**： AES67LINK GUI 与 VSC 虚拟声卡需要处于同一局域网，并选择同一张网络接口。

### 7.2 创建与管理 AES67 单播流

单播流用于在一台发送设备和一台接收设备之间建立点对点音频路由。可以把单播理解为“一对一发送”：指定哪台设备发送、哪台设备接收，其他设备不会接收这条音频流。

VSC 的单播流需要通过 AES67LINK GUI 控制软件创建和管理。

#### 7.2.1 使用 VSC 发送单播音频流

当需要把电脑中的声音发送到网络中的 AES67 设备时，可使用 VSC 发送单播音频流。

在 AES67LINK GUI 主路由界面中，左侧为发送设备，上方为接收设备。默认情况下，VSC 设备名类似 `vsc-xxxxx-xxxxx`。

操作步骤如下：

1. 在左侧发送设备列表中选择 VSC。
2. 将 VSC 的网络输出通道与目标接收设备的网络接收通道进行交叉选择。
3. 点击矩阵中的目标方块。
4. 当方块显示绿色勾号时，表示音频流创建成功。

创建成功后，VSC 对应通道的音频会发送到目标设备的接收通道。

下图示例中，`vsc-coffee` 的网络输出 1、2 通道分别发送到 AES67 Speaker 的网络接收 1、2 通道。

![vsc_send_unicast_audio_route](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/24-vsc_send_unicast_audio_route_zh.png)

#### 7.2.2 使用 VSC 接收单播音频流

当需要把网络中其他 AES67 设备的声音送入电脑时，可使用 VSC 接收单播音频流。VSC 接收单播流的方法与发送单播流类似，只需将接收设备设置为 VSC。

操作步骤如下：

1. 在左侧发送设备列表中选择需要发送音频的 AES67 设备。
2. 将发送设备的网络输出通道与 VSC 的网络接收通道进行交叉选择。
3. 点击矩阵中的目标方块。
4. 当方块显示绿色勾号时，表示音频流创建成功。

创建成功后，发送设备的音频会进入 VSC 的接收通道，电脑中的专业音频软件可通过 VSC 获取该声音。

下图示例中，AES67 Speaker 的网络输出 1、2 通道分别发送到 `vsc-coffee` 的网络接收 1、2 通道。

![vsc_receive_unicast_audio_route](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/25-vsc_receive_unicast_audio_route_zh.png)

#### 7.2.3 删除单播音频流

在 AES67LINK GUI 的 “设备路由” 界面中，点击已建立路由的绿色勾号。当绿色勾号消失时，表示该单播流订阅已取消，对应发送通道和接收通道之间的音频连接会断开。

### 7.3 创建与管理 AES67 组播流

组播流可用于一对多音频分发，也可用于与 Dante 等支持 AES67 的设备互通。可以把组播理解为“一台设备先把音频流发布到网络中，其他设备按需接收”。

如果同一组音频需要被多台设备接收，或者需要与 Dante 的 AES67 模式互通，通常需要使用组播流。VSC 的组播流需要通过 AES67LINK GUI 控制软件创建和管理。

#### 7.3.1 为 VSC 创建 AES67 组播流

1. 双击 VSC 设备名，打开 VSC 设备控制窗口。

![open_vsc_device_control_window](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/26-open_vsc_device_control_window_zh.png)

2. 在 VSC 设备控制窗口中，依次点击 “传输流” → “组播流”，进入组播流管理页面。在组播流管理页面中填写以下信息：

   - **组播流名称**：创建后显示的名称，长度不超过 32 个字符。建议使用容易识别的名称，方便后续路由和排查。

   - **目标地址**：组播流在网络中的接收地址。无特殊要求时建议使用自动分配，也可以手动指定地址。
   - **自动分配**：系统自动分配目标地址和端口号。目标地址会根据设备注册所在域配置的 RTP 前缀生成。例如 RTP 前缀为 69 时，系统会创建类似 `239.69.x.x` 的目标地址；默认端口号为 `5004`。如果不清楚如何设置组播地址，建议使用自动分配。
     
   - **自定义**：手动指定目标地址和端口。IP 地址必须位于 **239.0.0.0 ~ 239.254.254.254** 范围内，端口可设置为任意非管理端口号。只有在网络系统已有固定地址规划时，才建议手动填写。
   
   
      - **选择通道**：选择需要包含在组播流中的发送通道。
   


![create_multicast_stream_settings](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/27-create_multicast_stream_settings_zh.png)

创建完成后，可在左侧组播流统计区域确认组播流名称、IP 端口和已选择通道。能看到这些信息，说明组播流已经创建完成。

![multicast_stream_summary](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/28-multicast_stream_summary_zh.png)

创建好的组播流会在 “设备路由” 页面中以绿色方框显示，可按普通设备的方式进行路由。其他接收设备可以通过该组播流接收 VSC 发出的音频。

![multicast_stream_route_display](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/29-multicast_stream_route_display_zh.png)

#### 7.3.2 查看组播流详细信息

双击组播流名称区域，可打开组播流详细信息窗口。

![multicast_stream_detail_window](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/30-multicast_stream_detail_window_zh.png)

#### 7.3.3 删除组播流

选中需要删除的组播流，然后点击下方的 “删除” 按钮。

![delete_multicast_stream](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/31-delete_multicast_stream_zh.png)

### 7.4 使用 VSC 接收 AES67 组播流

VSC 支持接收标准 AES67 组播流。该功能适用于把其他 AES67 设备发布的组播音频送入 Windows 电脑。使用该功能需满足以下条件：

1. VSC 虚拟声卡版本为 **3.3.0.6** 或更高版本。
2. AES67LINK GUI 控制软件版本为 **3.3.0.6** 或更高版本。
3. VSC 虚拟声卡通道数为 **4 通道或以上**。
4. VSC 虚拟声卡音频接口设置为 **ASIO 模式**。

满足以上条件后，VSC 才能稳定接收网络中的 AES67 组播流。

![vsc_receive_multicast_stream](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/32-vsc_receive_multicast_stream_zh.png)

## 8. 问题排查

### 8.1 软件窗口显示过大

**现象：** 软件窗口显示过大，部分界面内容无法完整显示。

**原因：** Windows 系统显示缩放比例过大。

**处理方法：** 在 Windows 显示设置中降低缩放比例，或调整屏幕分辨率后重新打开软件。

### 8.2 软件安装时提示 `xxx.dll` 库缺失

**现象：** 安装或启动软件时提示缺少 `xxx.dll` 文件。

**原因：** 当前系统缺少 Microsoft Visual C++ 运行库。

**处理方法：** 下载并安装 Microsoft Visual C++ Redistributable。

- x64：[https://aka.ms/vs/17/release/vc_redist.x64.exe](https://aka.ms/vs/17/release/vc_redist.x64.exe)
- x86：[https://aka.ms/vs/17/release/vc_redist.x86.exe](https://aka.ms/vs/17/release/vc_redist.x86.exe)

### 8.3 软件启动失败并提示检查驱动

**现象：** VSC 软件启动失败，并提示检查驱动。

**原因：** VSC 驱动未正确安装或驱动状态异常。

**处理方法：** 在 Windows “设备管理器” 中检查 `DigisynAudio Virtual SoundCard` 的驱动状态。

1. 按下 `Win + R`，打开运行窗口。
2. 输入 `devmgmt.msc`，打开 “设备管理器”。

![open_windows_device_manager](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/39-open_windows_device_manager_zh.png)

3. 找到 `DigisynAudio Virtual SoundCard`。如果设备显示正常，说明驱动已正确安装；如果显示黄色感叹号，说明驱动异常。驱动异常时，可尝试重启电脑或重新安装 VSC 软件。

![vsc_driver_device_manager_status](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/40-vsc_driver_device_manager_status_zh.png)

### 8.4 Windows 声音设置中找不到 VSC 设备

**现象：** Windows 播放或录制设备列表中找不到 VSC 虚拟声卡。

**原因：** VSC 声音设备未正确启用，或当前查看的设备列表不完整。

**处理方法：** 打开 Windows “声音” 控制面板检查设备状态。

1. 按下 `Win + R`，打开运行窗口。
2. 输入 `mmsys.cpl`，打开 “声音” 控制面板。

![open_windows_sound_control_panel](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/41-open_windows_sound_control_panel_zh.png)

3. 在 “播放” 和 “录制” 页面中查看是否存在 VSC 设备。

![windows_playback_recording_vsc_devices](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/42-windows_playback_recording_vsc_devices_zh.png)

4. 如果 VSC 设备存在但处于禁用状态，右键点击该设备并选择启用。

![enable_disabled_vsc_sound_device](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/zh_image/43-enable_disabled_vsc_sound_device_zh.png)

### 8.5 激活虚拟声卡时提示网络错误

**现象：** 填写激活码并点击激活后，软件提示网络错误。

**可能原因：**

- Windows 防火墙拦截了 VSC 的激活请求。
- 当前网络环境异常或无法访问激活服务。
- 第三方杀毒软件或网络安全套件拦截了激活请求，例如 ESET、Norton、Kaspersky、360 等。

**处理方法：**

1. 检查 Windows 防火墙设置，确认 VSC 相关程序允许联网。
2. 检查当前网络环境，确认网络连接正常。
3. 暂时关闭或调整第三方安全软件的网络拦截策略，然后重新尝试激活。
