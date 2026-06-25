# AES67 VSC Virtual Sound Card User Manual

![VSC LOGO](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/01-vsc_logo_en.png)

The AES67 VSC Virtual Sound Card is suitable for Windows environments and can be used to transmit and receive AES67 network audio streams. It allows a Windows computer to connect to a network audio system just like an AES67 audio device.

AES67 is a universal protocol used for transmitting professional audio over a local area network (LAN). The discovery, routing, and management of audio streams require cooperation with the **AES67LINK GUI Control Software**. AES67LINK GUI is used to discover AES67 devices in the network and establish audio routing between transmitting channels and receiving channels.

AES67 VSC has been tested in a variety of mainstream network audio environments, including **RAVENNA**, **Dante**, **Q-LAN**, **Telos**, and **Crestron**.

## Product Features

- Supports **48 kHz, 96 kHz, 192 kHz** sample rates.
- Supports up to **64 x 64** channels.
- Supports Windows **WDM / ASIO** audio interfaces.

## Scope of Application

This document applies to the download, installation, activation, function settings, AES67 audio stream management, and troubleshooting of the Windows version of AES67 VSC. When reading this document, you can understand VSC as a "network audio device installed in the computer" and AES67LINK GUI as the "software used to connect various network audio devices."

## 1. Compatible System Versions

- When using the WDM audio interface, the system must be **Windows 10 22H2** or higher.
- When using the ASIO audio interface, the system must be **Windows 10** or higher.

## 2. Downloading and Installing the Virtual Sound Card

### 2.1 Downloading the Virtual Sound Card

Visit [https://docs.digisynthetic.com/](https://docs.digisynthetic.com/) and follow the path shown in the figure below to download the Windows installation package for the VSC Virtual Sound Card. After the download is complete, you should obtain an installer that can run on Windows.

![vsc_windows_download_path](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/03-vsc_windows_download_path_en.png)

### 2.2 Installing the Virtual Sound Card

1. Double-click the installation package and select the installation language. The installer supports Simplified Chinese and English.

![installer_language_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/04-installer_language_selection_en.png)

2. Choose whether to create a desktop shortcut and a Quick Launch shortcut as needed, and then click "Next".

![installer_shortcut_options](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/05-installer_shortcut_options_en.png)

3. Click "Install" and wait for the installer to complete. After installation, the VSC software and the corresponding virtual sound card driver will be installed on the computer.

![installer_ready_to_install](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/06-installer_ready_to_install_en.png)

**<font color="red">Note</font>**: If the Windows Firewall is enabled on your system, you need to allow `C:\Program Files (x86)\VSC\VSC.exe` and `C:\Program Files (x86)\VSC\myAudioRoute.exe` to access the network. Otherwise, the software may fail to activate, or it may not be able to discover and connect to AES67 devices in the network.

## 3. Language Switching

Click the "中 / En" button in the lower-left corner of the software to switch the interface language between Simplified Chinese and English.

![software_language_switch](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/07-software_language_switch_en.png)

## 4. Activating the Virtual Sound Card

After the installation is complete, the VSC Virtual Sound Card must be activated before it can be used. The software supports both online activation and offline activation.

### 4.1 Online Activation of Virtual Sound Card (Internet Connection Required)

Online activation is suitable for devices that can access the internet. This method is the simplest, as the software directly verifies the activation code via the network.

#### 4.1.1 Applying for an Online Activation Code

Visit [https://docs.digisynthetic.com/](https://docs.digisynthetic.com/) in a browser and register an official DOCS account. After successful registration, you can apply for a VSC online activation code in the lower-left corner of the page.

![docs_apply_online_activation_code](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/08-docs_apply_online_activation_code_en.png)

#### 4.1.2 Entering the Activation Code

After applying for the online activation code, return to the activation page of the VSC software and follow these steps to complete the activation:

1. Fill in the requested online activation code.
2. Click the "Activate" button.

After successful activation, the software will become available for use. You can then proceed to configure the network card, sample rate, channel count, and audio interface.

![vsc_online_activation](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/09-vsc_online_activation_en.png)

### 4.2 Offline Activation of Virtual Sound Card (No Internet Connection Required)

Offline activation is suitable for devices that cannot access the internet. This method requires exporting the local Machine ID first, and the manufacturer will generate an activation file specifically for this computer based on the Machine ID.

#### 4.2.1 Applying for an Offline Activation File

Copy the "Machine ID" displayed in the software and provide it to the manufacturer to generate the corresponding offline activation file. The Machine ID is used to identify the current computer, and different computers have different Machine IDs.

![offline_activation_machine_id](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/10-offline_activation_machine_id_en.png)

#### 4.2.2 Importing the Offline Activation File

After obtaining the activation file from the manufacturer, return to the activation page of the VSC software and follow these steps to complete the activation:

1. Select import certificate activation.
2. Select the `xxx_license.dat` file provided by the manufacturer.
3. Click "Open" in the lower right corner to complete the local offline activation.

After successful offline activation, the computer can use the VSC Virtual Sound Card in a network-free environment.

![select_offline_license_file](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/11-select_offline_license_file_en.png)

## 5. Main Function Settings

The main function settings of VSC include network card, sample rate, channel count, audio interface, and startup status. These parameters determine which network card VSC uses to transmit audio, how many audio channels are used, and which audio interface the computer software uses to call VSC.

After modifying critical parameters, it is recommended to restart the virtual sound card to make the configuration fully effective.

![main_function_settings](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/12-main_function_settings_en.png)

### 5.1 Network Card Selection

VSC needs to be bound to a physical wired network card actually used for AES67 network audio transmission. After binding the network card, VSC will transmit and receive AES67 audio streams through this card.

- Only physical wired network cards are supported.
- Virtual network cards or wireless network cards are not supported.
- If the computer has multiple physical network cards, you can expand the drop-down box to select the network card you want to use.

![network_adapter_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/13-network_adapter_selection_en.png)

The IPv4 address of the selected network card will be displayed in the "IP Address" area below.

![network_adapter_ip_address](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/14-network_adapter_ip_address_en.png)

**<font color="red">Note</font>**: Wireless networks are susceptible to signal strength, interference, and bandwidth fluctuations, which may cause audio dropouts, increased latency, or noise. Therefore, it is not recommended to use wireless network cards to transmit AES67 audio streams.

### 5.2 Sample Rate Selection

VSC supports selecting sample rates among **48 kHz, 96 kHz, 192 kHz**. The sample rate can be understood as the number of times audio is sampled and processed per second. The higher the sample rate, the larger the amount of audio data, and the higher the requirements for the computer and network.

![sample_rate_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/15-sample_rate_selection_en.png)

**<font color="red">Note</font>**: When interoperating with other AES67 or Dante devices, the sample rates of the relevant devices must remain consistent. If the sample rates are inconsistent, routing may fail to establish, or there may be no sound after establishment.

### 5.3 Channel Count Selection

The number of input and output channels of the VSC Virtual Sound Card can be set according to the authorization scope. The channel count determines the maximum number of audio signals the computer can transmit or receive simultaneously.

- The online activation code requested on [https://docs.digisynthetic.com/](https://docs.digisynthetic.com/) defaults to an 8-channel authorization, meaning both input and output channel counts are 8.
- If more channels are required, please contact the manufacturer to obtain the corresponding authorization.

![channel_count_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/16-channel_count_selection_en.png)

**<font color="red">Note</font>**: The greater the number of channels, the more audio data is processed simultaneously, and the higher the performance requirements for the Windows computer. If the computer performance is insufficient, audio stuttering or noise may occur.

### 5.4 Audio Interface Selection

VSC supports two audio interfaces: **WDM** and **ASIO**. The audio interface determines how the software in the computer uses VSC.

1. **WDM**: Visible in Windows system sound devices, suitable for general playback, recording, and system sound scenarios, such as Wasapi, WaveOut, DirectSound, etc.
2. **ASIO**: Usually not displayed in Windows system sound devices, suitable for direct invocation by professional audio software, such as Reaper, Adobe Audition, etc.

The time after the ASIO option represents the buffer size, which is the audio latency. The smaller the value, the lower the audio latency; however, the computer needs to process audio data faster, requiring higher stability.

![audio_interface_selection](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/17-audio_interface_selection_en.png)

**<font color="red">Note</font>**: When using low-latency ASIO playback, if noise, pops, or audio dropouts occur, please appropriately increase the ASIO latency. Increasing latency will slightly increase sound delay but can generally improve playback stability.

### 5.5 Starting the Virtual Sound Card

After completing the parameter settings, you need to start the virtual sound card channels to use the VSC function normally. Once started, VSC will begin working as a network audio device and can be discovered by AES67LINK GUI.

- When selecting the WDM audio interface, you need to wait for all system channels to complete initialization before use.
- When selecting the ASIO audio interface, it can usually be used directly.

![start_virtual_soundcard](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/18-start_virtual_soundcard_en.png)

### 5.6 Using VSC as Input and Output Devices

In Windows "System Settings" → "Volume" → "Volume Mixer", you can select VSC as the input device (recording) or output device (playback). For example, after selecting VSC as the output device, the playback sound from the computer can enter VSC and then be sent to other audio devices in the network via AES67 routing.

![windows_sound_output_input_device](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/19-windows_sound_output_input_device_en.png)

## 6. Other Settings

This page contains additional parameter settings for VSC. These settings usually do not need to be modified frequently and are adjusted only when the network audio system has specific requirements.

**<font color="red">Note</font>**: After modifying the settings on this page, you must click "Save" for them to take effect.

![other_settings_save_button](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/20-other_settings_save_button_en.png)

### 6.1 Setting PTP Domain (Clock Domain)

You can set the PTP Domain where the AES67 VSC Virtual Sound Card is located here. PTP is used to allow network audio devices to use the same time reference, preventing playback speed or time out-of-sync between different devices.

A PTP Domain can be understood as a "clock synchronization group". Only devices in the same PTP Domain will synchronize clocks with each other.

- If the virtual sound card has already been started, you need to restart the virtual sound card after modifying the PTP Domain.
- For the method of restarting the virtual sound card, see "5.5 Starting the Virtual Sound Card".

![ptp_domain_setting](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/21-ptp_domain_setting_en.png)

**<font color="red">Note</font>**: Due to the clock accuracy limitations of Windows, the VSC Virtual Sound Card can only follow other master clock devices and cannot serve as the master clock for the entire AES67 system.

## 7. Discovering and Using the Virtual Sound Card

The actual audio stream management of AES67 VSC needs to be completed in conjunction with the AES67LINK GUI control software. AES67 VSC is responsible for turning the computer into an AES67 audio device, and AES67LINK GUI is responsible for establishing audio connections between AES67 VSC and other AES67 devices.

The AES67LINK GUI control software can be downloaded from [https://docs.digisynthetic.com/](https://docs.digisynthetic.com/).

![aes67link_download_path](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/22-aes67link_download_path_en.png)

### 7.1 Discovering VSC in AES67LINK GUI

Regardless of whether VSC uses the WDM or ASIO audio interface, after starting the virtual sound card, it can be discovered and controlled in AES67LINK GUI. Upon successful discovery, VSC will be displayed in the device list or routing interface of AES67LINK GUI just like other network audio devices.

![aes67link_discover_vsc_device](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/23-aes67link_discover_vsc_device_en.png)

**<font color="red">Note</font>**: AES67LINK GUI and the VSC Virtual Sound Card must be in the same local area network (LAN) and select the same network interface.

### 7.2 Creating and Managing AES67 Unicast Streams

Unicast streams are used to establish point-to-point audio routing between a transmitting device and a receiving device. Unicast can be understood as "one-to-one transmission": specifying which device transmits and which device receives, and other devices will not receive this audio stream.

Unicast streams for VSC need to be created and managed via the AES67LINK GUI control software.

#### 7.2.1 Transmitting Unicast Audio Streams Using VSC

When you need to send sound from the computer to AES67 devices in the network, you can use VSC to transmit unicast audio streams.

In the main routing interface of AES67LINK GUI, the left side shows the transmitting devices, and the top shows the receiving devices. By default, the VSC device name resembles `vsc-xxxxx-xxxxx`.

Steps are as follows:

1. Select VSC from the transmitting device list on the left.
2. Cross-select the network output channels of VSC with the network receiving channels of the target receiving device.
3. Click the target square in the matrix.
4. When a green check mark appears in the square, it indicates the audio stream has been successfully created.

After successful creation, the audio from the corresponding channels of VSC will be sent to the receiving channels of the target device.

In the example below, network output channels 1 and 2 of `vsc-coffee` are transmitted to network receiving channels 1 and 2 of the AES67 Speaker respectively.

![vsc_send_unicast_audio_route](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/24-vsc_send_unicast_audio_route_en.png)

#### 7.2.2 Receiving Unicast Audio Streams Using VSC

When you need to bring sound from other AES67 devices in the network into the computer, you can use VSC to receive unicast audio streams. The method for VSC to receive a unicast stream is similar to transmitting one, except you set VSC as the receiving device.

Steps are as follows:

1. Select the AES67 device that needs to transmit audio from the transmitting device list on the left.
2. Cross-select the network output channels of the transmitting device with the network receiving channels of VSC.
3. Click the target square in the matrix.
4. When a green check mark appears in the square, it indicates the audio stream has been successfully created.

Upon successful creation, the audio from the transmitting device will enter the receiving channels of VSC, and professional audio software on the computer can obtain the sound via VSC.

In the example below, network output channels 1 and 2 of the AES67 Speaker are transmitted to network receiving channels 1 and 2 of `vsc-coffee` respectively.

![vsc_receive_unicast_audio_route](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/25-vsc_receive_unicast_audio_route_en.png)

#### 7.2.3 Deleting Unicast Audio Streams

In the "Device Routing" interface of AES67LINK GUI, click the green check mark of the established route. When the green check mark disappears, it indicates that the unicast stream subscription has been canceled, and the audio connection between the corresponding transmitting channel and receiving channel will be disconnected.

### 7.3 Creating and Managing AES67 Multicast Streams

Multicast streams can be used for one-to-many audio distribution and can also be used to interoperate with AES67-supporting devices like Dante. Multicast can be understood as "a device first publishes an audio stream to the network, and other devices receive it as needed."

If the same audio group needs to be received by multiple devices, or needs to interoperate with Dante's AES67 mode, multicast streams are usually required. Multicast streams for VSC must be created and managed via the AES67LINK GUI control software.

#### 7.3.1 Creating an AES67 Multicast Stream for VSC

1. Double-click the VSC device name to open the VSC device control window.

![open_vsc_device_control_window](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/26-open_vsc_device_control_window_en.png)

2. In the VSC device control window, click "Transmit Streams" → "Multicast Streams" in sequence to enter the multicast stream management page. Fill in the following information on the multicast stream management page:

   - **Multicast Stream Name**: The name displayed after creation, with a length of no more than 32 characters. It is recommended to use an easily recognizable name to facilitate subsequent routing and troubleshooting.

   - **Destination Address**: The receiving address of the multicast stream in the network. If there are no special requirements, it is recommended to use automatic allocation, or you can manually specify the address.
   
   - **Automatic Allocation**: The system automatically allocates the destination address and port number. The destination address is generated based on the RTP prefix configured in the domain where the device is registered. For example, when the RTP prefix is 69, the system creates a destination address similar to `239.69.x.x`; the default port number is `5004`. If you do not know how to set up the multicast address, it is recommended to use automatic allocation.
     
   - **Custom**: Manually specify the destination address and port. The IP address must be within the range of **239.0.0.0 ~ 239.254.254.254**, and the port can be set to any non-managed port number. It is recommended to fill it out manually only when the network system already has a fixed address plan.
   
   - **Select Channels**: Select the transmitting channels to be included in the multicast stream.

![create_multicast_stream_settings](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/27-create_multicast_stream_settings_en.png)

After the creation is complete, you can confirm the multicast stream name, IP port, and selected channels in the multicast stream statistics area on the left. Seeing this information indicates that the multicast stream has been successfully created.

![multicast_stream_summary](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/28-multicast_stream_summary_en.png)

The created multicast stream will be displayed as a green box on the "Device Routing" page and can be routed in the same way as common devices. Other receiving devices can receive the audio emitted by VSC through this multicast stream.

![multicast_stream_route_display](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/29-multicast_stream_route_display_en.png)

#### 7.3.2 Viewing Multicast Stream Details

Double-click the multicast stream name area to open the multicast stream details window.

![multicast_stream_detail_window](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/30-multicast_stream_detail_window_en.png)

#### 7.3.3 Deleting Multicast Streams

Select the multicast stream you want to delete, and then click the "Delete" button below.

![delete_multicast_stream](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/31-delete_multicast_stream_en.png)

### 7.4 Receiving AES67 Multicast Streams Using VSC

VSC supports receiving standard AES67 multicast streams. This feature is suitable for bringing multicast audio published by other AES67 devices into a Windows computer. To use this feature, the following conditions must be met:

1. The VSC Virtual Sound Card version must be **3.3.0.6** or higher.
2. The AES67LINK GUI control software version must be **3.3.0.6** or higher.
3. The VSC Virtual Sound Card channel count must be **4 channels or more**.
4. The VSC Virtual Sound Card audio interface must be set to **ASIO mode**.

Once the above conditions are met, VSC can stably receive AES67 multicast streams from the network.

![vsc_receive_multicast_stream](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/32-vsc_receive_multicast_stream_en.png)

## 8. Troubleshooting

### 8.1 Software Window Displaying Too Large

**Symptom:** The software window is displayed too large, and part of the interface content cannot be fully shown.

**Reason:** The Windows system display scaling ratio is set too high.

**Resolution:** Lower the scaling ratio in Windows display settings, or adjust the screen resolution, and then reopen the software.

### 8.2 Error Prompting Missing `xxx.dll` Library During Installation

**Symptom:** A prompt indicates that a `xxx.dll` file is missing during software installation or startup.

**Reason:** The current system lacks the Microsoft Visual C++ Redistributable runtime.

**Resolution:** Download and install the Microsoft Visual C++ Redistributable.

- x64: [https://aka.ms/vs/17/release/vc_redist.x64.exe](https://aka.ms/vs/17/release/vc_redist.x64.exe)
- x86: [https://aka.ms/vs/17/release/vc_redist.x86.exe](https://aka.ms/vs/17/release/vc_redist.x86.exe)

### 8.3 Software Startup Fails and Prompts to Check Driver

**Symptom:** The VSC software fails to start and prompts to check the driver.

**Reason:** The VSC driver is not correctly installed or the driver status is abnormal.

**Resolution:** Check the driver status of `DigisynAudio Virtual SoundCard` in Windows "Device Manager".

1. Press `Win + R` to open the Run window.
2. Type `devmgmt.msc` and open "Device Manager".

![open_windows_device_manager](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/39-open_windows_device_manager_en.png)

3. Find `DigisynAudio Virtual SoundCard`. If the device displays normally, it indicates the driver is correctly installed; if a yellow exclamation mark is shown, the driver is abnormal. In case of a driver anomaly, try restarting the computer or reinstalling the VSC software.

![vsc_driver_device_manager_status](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/40-vsc_driver_device_manager_status_en.png)

### 8.4 VSC Device Cannot Be Found in Windows Sound Settings

**Symptom:** The VSC Virtual Sound Card cannot be found in the Windows playback or recording device list.

**Reason:** The VSC sound device is not properly enabled, or the currently viewed device list is incomplete.

**Resolution:** Open the Windows "Sound" control panel to check the device status.

1. Press `Win + R` to open the Run window.
2. Type `mmsys.cpl` and open the "Sound" control panel.

![open_windows_sound_control_panel](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/41-open_windows_sound_control_panel_en.png)

3. Check whether the VSC device exists on the "Playback" and "Recording" pages.

![windows_playback_recording_vsc_devices](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/42-windows_playback_recording_vsc_devices_en.png)

4. If the VSC device exists but is disabled, right-click the device and select Enable.

![enable_disabled_vsc_sound_device](https://docs.digisynthetic.com/uploads/VSC_Manual/Windows/en_image/43-enable_disabled_vsc_sound_device_en.png)

### 8.5 Network Error Prompted When Activating the Virtual Sound Card

**Symptom:** After filling in the activation code and clicking activate, the software prompts a network error.

**Possible Reasons:**

- Windows Firewall blocked VSC's activation request.
- The current network environment is abnormal or cannot access the activation service.
- Third-party antivirus software or network security suites blocked the activation request, such as ESET, Norton, Kaspersky, 360, etc.

**Resolution:**

1. Check Windows Firewall settings to confirm that VSC-related programs are allowed to access the network.
2. Check the current network environment to confirm the network connection is normal.
3. Temporarily close or adjust the network blocking policies of third-party security software, and then try to activate again.
