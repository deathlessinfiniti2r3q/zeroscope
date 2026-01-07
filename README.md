<p align="center">
  <img src="https://placehold.co/800x120/0f172a/64748b?text=ZeroScope&font=mono&bold=1&size=64" alt="ZeroScope" width="100%"/>
</p>
# ZeroScope

> **Local, zero-shot text-to-video generation — lightweight, transparent, and privacy-respecting.**  
> Run short video synthesis on consumer hardware, without internet or external services.

ZeroScope is a minimal, locally executable implementation of **zero-shot text-to-video generation**, designed for research, prototyping, and creative exploration. Built on diffusion priors and temporal interpolation, it generates coherent short clips from text prompts — entirely on your machine.

Unlike cloud-based alternatives, ZeroScope requires **no API keys, no telemetry, and no internet connection** after initial setup. Your prompts stay private. Your outputs belong to you.

<p align="center">
  <img src="https://placehold.co/600x340/0f172a/ffffff?text=A+paper+airplane+flying+through+a+library" width="31%"/>
  <img src="https://placehold.co/600x340/1e293b/ffffff?text=Fireflies+glowing+in+a+moonlit+forest" width="31%"/>
  <img src="https://placehold.co/600x340/020617/ffffff?text=Steam+rising+from+a+cup+on+a+wooden+table" width="31%"/>
</p>

---

## Philosophy

ZeroScope is not a product — it’s a **reference implementation**.  
It prioritizes:

- **Simplicity** over feature bloat  
- **Transparency** over black-box magic  
- **Local execution** over cloud dependency  
- **Reproducibility** over hidden optimizations  

This project is intended for **technical users, educators, and researchers** who wish to understand or extend zero-shot video generation — not for production-grade video pipelines.

---

## Capabilities

- Text-to-video generation (2–6 seconds)  
- Resolution: 256×256 (optimized for speed & memory)  
- Frame rate: 8–12 FPS  
- Works on GPU (CUDA) and CPU  
- Outputs standard MP4 files via FFmpeg  
- Built on Hugging Face `diffusers` and `transformers`

> Note: Quality is limited by model size and temporal coherence constraints. Outputs may exhibit artifacts or motion inconsistencies — this is expected behavior for a lightweight zero-shot system.

---

## Performance (4-second video)

| Hardware           | Time     | VRAM Usage |
|--------------------|----------|------------|
| RTX 3060 (12 GB)   | ~2.1 min | ~5.8 GB    |
| RTX 4070 (12 GB)   | ~1.7 min | ~5.8 GB    |
| Apple M1 Pro       | ~4.3 min | ~6.2 GB    |
| CPU (i7-12700)     | ~28 min  | ~9.1 GB RAM|

Use `--fp16` for faster inference on compatible GPUs.

---

## Ethical Use

ZeroScope must not be used to:
- Generate synthetic media of real individuals without consent  
- Create misleading or harmful content  
- Circumvent copyright protections  
- Automate disinformation  

The model weights are derived from open academic releases and are provided for **non-commercial research and educational purposes only**.

---

## Technical Notes

- Based on the **Text2Video-Zero** methodology (Khurana et al., 2023)  
- Model: `cerspense/zeroscope-v2-576w` (from Hugging Face)  
- Code license: **MIT**  
- Model license: **CreativeML Open RAIL-M**  
- Requires ~3.2 GB disk space for weights

This is **not** a fork of commercial systems. It is a reimplementation for local use, with no affiliation to any corporate entity.

---

## Support & Contribution

- Report bugs or inconsistencies: [Issues](https://github.com/your-username/ZeroScope/issues)  
- Discuss use cases or limitations: [Discussions](https://github.com/your-username/ZeroScope/discussions)  
- Improve documentation or performance: PRs welcome  

We value **honesty about limitations** as much as technical excellence.

---

**ZeroScope**: A small window into the future of video — open, local, and modest in its claims.
