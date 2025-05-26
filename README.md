[![zh](https://img.shields.io/badge/lang-zh-blue.svg)](./README.zh.md)

<!-- PROJECT LOGO -->
<br />
<div align="center">
    <a href="https://github.com/PlayForDreamDevelopers/DreamOSConfigs">
        <img src="https://www.pfdm.cn/en/static/img/logo.2b1b07e.png" alt="Logo" width="20%">
    </a>
    <h1 align="center"> Dream OS Configuration Files </h1>
    <p align="center">
        A collection of configuration files for Dream OS
        <br />
        <a href="https://www.pfdm.cn/yvrdoc/biz/docs/SystemCustomizationSolution.html"><strong>View Documentation »</strong></a>
        <br />
        <br />
        <a href="https://github.com/PlayForDreamDevelopers/DreamOSConfigs/issues/new?template=bug_report.yml">Report Bug</a>
        &middot;
        <a href="https://github.com/PlayForDreamDevelopers/DreamOSConfigs/issues/new?template=feature_request.yml">Request Feature</a>
        &middot;
        <a href="https://github.com/PlayForDreamDevelopers/DreamOSConfigs/issues/new?template=documentation_update.yml">Improve Documentation</a>
    </p>
</div>

> [!tip]
>
> Currently, only Play for Dream MR devices support Dream OS free configuration.

## About the Project

Dream OS on Play For Dream MR devices opens up configuration capabilities for certain applications. You can customize the system by modifying configuration files.

By convention, configuration files for each application are stored in the `/sdcard/misc/dreamos/<packageName>` directory. For example, for the *Eye Calibration* app, its configuration files are stored in `/sdcard/misc/dreamos/com.yvr.eyecalibration`.

You can copy the Eye Calibration app's configuration file to your device as follows:

```bash
adb shell mkdir -p /sdcard/misc/dreamos/com.yvr.eyecalibration # Create directory
adb push <CaliConfig.json Path> /sdcard/misc/dreamos/com.yvr.eyecalibration # Push file to device, replace <CaliConfig.json Path> with the actual path on your PC
adb reboot # Restart device
```

For details on the format and content of each application's configuration file, please refer to the [Dream OS Configuration File Documentation](https://www.pfdm.cn/yvrdoc/bizen/docs/SystemCustomizationSolution.html).