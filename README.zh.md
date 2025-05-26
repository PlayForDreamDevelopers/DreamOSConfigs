[![us](https://img.shields.io/badge/lang-us-red.svg)](./README.md)

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/PlayForDreamDevelopers/DreamOSConfigs">
    <img src="https://www.pfdm.cn/en/static/img/logo.2b1b07e.png" alt="Logo" width="20%">
  </a>

  <h1 align="center"> Dream OS 配置文件 </h1>

  <p align="center">
    Dream OS 的配置文件集合
    <br />
    <a href="https://www.pfdm.cn/yvrdoc/biz/docs/SystemCustomizationSolution.html"><strong>查看文档 »</strong></a>
    <br />
    <br />
    <a href="https://github.com/PlayForDreamDevelopers/DreamOSConfigs/issues/new?template=bug_report.yml">报告错误</a>
    &middot;
    <a href="https://github.com/PlayForDreamDevelopers/DreamOSConfigs/issues/new?template=feature_request.yml">请求功能</a>
    &middot;
    <a href="https://github.com/PlayForDreamDevelopers/DreamOSConfigs/issues/new?template=documentation_update.yml">改进文档</a>
    
  </p>
</div>

> [!tip]
>
> 目前，仅 Play for dream MR 设备支持 Dream OS 自由配置
 
## 关于项目

Play For Dream MR 的 Dream OS 系统开放了部分应用的自由配置功能，你可以通过修改配置文件来定制系统。

我们约定各应用的配置文件都存放在 `/sdcard/misc/dreamos/<packageName>` 目录下。例如针对 *眼动校准* 应用，其配置文件存放在 `/sdcard/misc/dreamos/com.yvr.eyecalibration` 目录下。

你可以将通过如下的方式将眼动校准应用的配置文件复制到设备上：

```bash
adb shell mkdir -p /sdcard/misc/dreamos/com.yvr.eyecalibration # Create directory
adb push <CaliConfig.json Path> /sdcard/misc/dreamos/com.yvr.eyecalibration # Push file to device, replace <CaliConfig.json Path> with the actual path on your PC
adb reboot # Restart device
```

关于各应用的配置文件格式和内容，请参考 [Dream OS 配置文件文档](https://www.pfdm.cn/yvrdoc/biz/docs/SystemCustomizationSolution.html)。