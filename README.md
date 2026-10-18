
<div align="center">

# Luomic Blog
![](./docs/images/kazuha.png)

![Node.js >= 22](https://img.shields.io/badge/node.js-%3E%3D22-brightgreen) 
![pnpm >= 11](https://img.shields.io/badge/pnpm-%3E%3D9-blue)
![Astro](https://img.shields.io/badge/Astro-7-orange)
![TypeScript](https://img.shields.io/badge/TypeScript-6-blue)

</div>


---

## 🚀 快速开始

### 环境要求

- Node.js ≥ 22
- pnpm ≥ 11

### 本地开发部署

1. **克隆仓库：**
   ```bash
   git clone https://github.com/Luomic/LuoBlog.git
   cd LuoBlog
   ```

3. **安装依赖：**
   ```bash
   # 如果没有安装 pnpm，先安装
   npm install -g pnpm
   
   # 安装项目依赖
   pnpm install
   ```

4. **配置博客：**
   - 编辑 `src/config/` 目录下的配置文件自定义博客设置

5. **启动开发服务器：**
   ```bash
   pnpm dev
   ```
   博客将在 `http://localhost:4321` 可用

### 平台托管部署
- **参考[官方指南](https://docs.astro.build/zh-cn/guides/deploy/)将博客部署至 Vercel, Netlify, Cloudflare Pages, EdgeOne Pages 等。**
- **Vercel**、**Netlify** 等主流平台自动部署，会根据环境自动选择适配器。

   框架预设： `Astro`

   根目录： `./`

   输出目录： `dist`

   构建命令： `pnpm run build`

   安装命令： `pnpm install`

   [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/CuteLeaf/Firefly&project-name=Firefly&repository-name=Firefly)
   [![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/CuteLeaf/Firefly)

## 🙏 致谢

### 技术栈

- [Astro](https://astro.build) 
- [Tailwind CSS](https://tailwindcss.com) 
- [Iconify](https://iconify.design)

## 📝 许可协议

本项目遵循 [MIT license](https://mit-license.org/) 开源协议，详细查看 [LICENSE](./LICENSE) 文件

最初 Fork 自 [saicaca/fuwari](https://github.com/saicaca/fuwari)，感谢原作者的贡献

**版权声明：**
- Copyright (c) 2024 [saicaca](https://github.com/saicaca) - [fuwari](https://github.com/saicaca/fuwari)
- Copyright (c) 2025 [CuteLeaf](https://github.com/CuteLeaf) - [Firefly](https://github.com/CuteLeaf/Firefly) 

根据 MIT 开源协议，你可以自由使用、修改、分发代码，但需保留上述版权声明。


<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
