# Gints Golubs

Technical Coordinator / Developer at [EdgeOptic](https://edgeoptic.com), an optical networking
hardware company · Riga, Latvia

I work across web development, AI integration in the company's processes, and technical support
for optical transceivers down to EEPROM data and DDM readings. Most of that work lives in private
company repositories. The project below is public.

## local-llm-bench

**[Gincha0/local-llm-bench](https://github.com/Gincha0/local-llm-bench)** · Python, Ollama, Linux, AWS

The same eight local LLM builds (Qwen3 0.6B to 8B, each as Q4_K_M and Q8_0) run on four device
tiers: an RTX 4070 desktop, the same machine CPU-only, an RTX 4060 laptop on Windows, and a 4 GB
ARM cloud VM. It measures time to first token, prompt and generation speed, memory and output
correctness: 860 measured requests, each tied to a record of the hardware, software and commit
that produced it.

- Generation speed is set by memory bandwidth. The 8B Q8 model ran at 95 % of the RTX 4070's
  504 GB/s, and the laptop GPU, with about half that bandwidth, ran at about half the speed.
- A model split between VRAM and system RAM loses most of the GPU's advantage: 8B Q8 on the 8 GB
  laptop GPU ran 3.5× slower than 8B Q4, and only 1.6× faster than the desktop's CPU alone.
- On two ARM cores the bandwidth rule breaks and Q8 is faster than Q4.
- On the 4 GB VM, `llama-server`'s default prompt cache grew until the kernel killed the server
  for lack of memory, while Ollama reported 1.7 GiB in use.

## Work at EdgeOptic (since 2023)

- Skill set behind the company's Slack AI agent: employees create configurable products and
  solution pages and manage internal linking through it, and every change is previewed and
  approved before it is written
- Internal-linking system for the 6,000-product catalogue: similar-product groups, upsells and
  two-way links between products and the articles that mention them, run through the same agent
- WDM multiplexer configurator for 43 product families, with live front-panel previews
  (Next.js, Sanity)
- [Solution pages](https://edgeoptic.com/solutions): topology diagrams with clickable product pins
  and a parts list built from them
- Co-built the front end of edgeoptic.com's move from WordPress/WooCommerce to Next.js and Sanity

## Stack

- **Python:** pydantic, httpx, pytest, matplotlib, uv, ruff, mypy
- **LLMs:** Ollama, llama.cpp, GGUF quantisation, agent skill and tool design
- **Web:** TypeScript, Next.js, React, Tailwind CSS, Sanity CMS
- **Linux and tooling:** CachyOS as daily driver, SSH, systemd, tmux, git (Conventional Commits), AWS EC2
- **Also:** C++ (coursework), PowerShell, BettyBlocks (low-code)

## Other projects

- [CONVEX Brand Site](https://github.com/Gincha0/Convex_Brand_site): brand site for a PC case
  design concept, built to practise animation sequences and component architecture (Next.js,
  TypeScript, Tailwind CSS, Framer Motion)

## Currently

- Learning Python in depth
- IT/Programming associate degree at Alberta College, Riga (expected 2027)

## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/gints-golubs-769744229)
[![Email](https://img.shields.io/badge/Email-ggolubs%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ggolubs@gmail.com)
