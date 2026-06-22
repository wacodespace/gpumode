# GPU Mode / SGLang AI Infra Slides

这个仓库收集了一组和 SGLang AI Infra、GPU Mode 相关的技术分享 slides。

这些内容主要来自我对 GPU 编程、AI Infra、SGLang、NCCL、PTX/SASS 等主题的学习和整理：我把原本的分享材料转成了 HTML 页面，并在其中补充了一些自己的理解、观察和延伸思考。它更像是一个技术阅读与分享笔记库，而不是一个需要编译运行的软件项目。

## 内容结构

```text
.
├── new_nccl/
│   └── NCCL、新通信特性、NIXL、KV cache offload 等相关 slides
├── ptx_sass_level_review/
│   └── PTX/SASS、GPU 汇编阅读、性能分析和硬件视角相关 slides
└── sglang_relative/
    └── SGLang 相关实现细节和调用链分析
```

## 主要主题

- SGLang 与 AI Infra 中的关键实现路径
- NCCL 通信机制、API、kernel、容错和性能相关内容
- NIXL、KV cache offload、disaggregated serving 等系统方向
- PTX 与 SASS 的关系，以及从汇编层理解 GPU kernel
- Nsight Compute、binary 分析、硬件行为和性能调优视角
- 我在阅读这些材料时记录下来的理解、疑问和感悟

## 如何阅读

每个 slide 都是独立的 HTML 文件，可以直接用浏览器打开：

```bash
open new_nccl/nccl_ep_api_slide.html
open ptx_sass_level_review/ptx-vs-sass.html
open sglang_relative/kv_cache_dtype_callchain.html
```

也可以在仓库根目录启动一个简单的静态文件服务器：

```bash
python3 -m http.server 8000
```

然后在浏览器里访问：

```text
http://localhost:8000
```

## 说明

这些 slides 主要用于个人学习、复盘和技术分享。部分内容是对公开技术材料、源码阅读和工程实践的二次整理，仓库中的注释和表达会带有较强的个人理解色彩。

如果你也在关注 SGLang、GPU Mode、NCCL 或 GPU kernel 性能分析，希望这些页面能作为一个按主题整理过的入口。
