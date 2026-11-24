# H3 有声短剧

一个面向 Codex 的中文 Skill。把剧本拆成因果连贯的镜头，用 MiniMax H3 的 I2V 拍动作，用 R2V 参考定妆和试音，制作跨镜头角色一致的有声短剧。

## 安装

```bash
npx skills add Kayshen-X/h3-short-drama --skill h3-short-drama -a codex
```

手动安装时，把 [h3-short-drama 目录](skills/h3-short-drama) 复制到项目的 `.agents/skills/` 中。

## 一句话调用

> 用 `$h3-short-drama` 把这个故事拍成有声短剧，让每个转折都有看得见的动作，用 I2V 衔接镜头、用 R2V 延续角色外形和声线，再按选定的 H3 原声对口型。

把故事、定妆图或已有素材一并交给 Codex。实际渲染需要可访问的 ComfyUI 和对应的 H3 权重。已有完整镜头时，也可以只指定一处要修的对白或转场。

## I2V 和 R2V 怎么选

- **I2V** 从指定首帧起拍。适合手机落桌、递合同等起始位置已经确定的动作，对应 H3 的 `fl2va` 权重。
- **R2V** 让新镜头参考图片、视频或音频。适合换场后复用角色定妆和声线，对应 `ref2va` 权重。为每个说话人单独标明参考音色和本镜台词。

完整的选镜、试音和导出流程见 [SKILL.md](skills/h3-short-drama/SKILL.md)。节点和模型配置见 [ComfyUI 官方 H3 文档](https://docs.comfy.org/tutorials/video/minimax/minimax-h3-native)。

本仓库的 Skill 与文档采用 [MIT 许可证](LICENSE)。
