# Prun-TTS: Let Speak with Fewer but Essential Layers

This repository contains the demo webpage for **Prun-TTS**, a compression and distillation framework for efficient Large Language Model (LLM)-based Text-to-Speech systems.

## 🎯 Overview

Prun-TTS addresses the computational challenges of modern LLM-based TTS systems like CosyVoice and LLaSA by introducing a novel pruning and distillation framework that significantly reduces model complexity while maintaining high audio quality.

## 🌟 Key Results

- **50%** Model Depth Reduction
- **20%** VRAM Usage Reduction  
- **<5%** Training Data Required

## 👥 Authors

- [Tan Dat Nguyen](https://signofthefour.github.io/) - Korea Advanced Institute of Science and Technology (KAIST)
- [Ji-Hoon Kim](https://sites.google.com/view/jhoonkim/) - Korea Advanced Institute of Science and Technology (KAIST)
- [Jaehun Kim](https://smokedindia.notion.site/Jaehun-Kim-5006f1fc98004817885325241723f1e3) - Korea Advanced Institute of Science and Technology (KAIST)
- [Joon Son Chung](https://mmai.io/joon/)† - Korea Advanced Institute of Science and Technology (KAIST)

†Corresponding author

## 🔬 Abstract

The goal of this paper is to develop a compression and distillation framework for efficient Large Language Model (LLM)-based Text-to-Speech (LLM-TTS) systems. Recent advances such as CosyVoice and LLaSA have demonstrated strong improvements in controllability, prosody modeling, and cross-speaker generalization. However, their large parameter counts, high memory consumption, and slow inference limit practical deployment. 

Our framework integrates a *pruning* step to identify and remove redundant layers with a *distillation* process that transfers knowledge from the teacher model, thereby preserving semantic fidelity. Experiments on zero-shot synthesis benchmarks shows that the proposed framework achieves near-parity with LLaSA while reducing LLM model depth by **50%** and VRAM usage by **20%**, requiring less than **5%** of the original training data. These results demonstrate that compact LLM-TTS models can retain high fidelity while enabling practical, resource-efficient speech generation.

## 🎵 Audio Demos

The demo webpage features interactive audio comparisons between:

- **Ground Truth** - Original reference audio
- **CosyVoice 2** - Baseline CosyVoice model
- **CosyVoice 2 Lite** - Compressed CosyVoice variant
- **LLaSA** - Large Language Audio model
- **LLaSA Lite (Ours)** - Our pruned and distilled model

### Audio Controls

- 🎵 **Play All** - Play all audio samples simultaneously
- ⏸️ **Pause All** - Pause all playing audio
- ⏹️ **Stop All** - Stop and reset all audio

## 🛠️ Demo Website Features

### Modern UI Framework

- **Bulma CSS** - Modern CSS framework for responsive design
- **FontAwesome Icons** - Professional iconography
- **Interactive Components** - Carousels, sliders, and audio controls
- **Responsive Design** - Mobile-friendly layout

### Navigation

- 🏠 **Home Button** - Links to Multimodal AI Lab - KAIST (with rounded corners)
- 📄 **arXiv Paper** - Direct link to research paper
- 💻 **Code Repository** - GitHub source code access
- 🔬 **More Research** - Additional publications from the lab

### Visual Design

- **Green Navigation Bar** - Professional branding
- **White Hero Section** - Clean, readable title area
- **Interactive Audio Table** - Striped, hoverable rows with highlighted "Ours" column
- **Key Results Showcase** - Prominent display of main achievements
- **Method Overview Images** - Visual explanation of the approach

## 📁 Project Structure

```text
pruntts/
├── index.html              # Main demo webpage
├── README.md               # This file
├── audio/                  # Audio sample directories
│   ├── codec/             # Codec processed audio
│   ├── cosyvoice_heal/    # CosyVoice 2 samples
│   ├── cosyvoice_ref/     # CosyVoice 2 Lite samples
│   ├── gt/                # Ground truth audio
│   ├── llasa_heal/        # LLaSA samples
│   ├── llasa_ref/         # LLaSA Lite (Ours) samples
│   └── vocoder/           # Vocoder processed audio
├── images/                # Method overview figures
│   ├── 1.png
│   ├── 2.png
│   └── 3.png
└── static/                # Web assets
    ├── audio_paths.json   # Audio file mappings
    ├── css/               # Stylesheets
    │   ├── bulma.min.css
    │   ├── bulma-carousel.min.css
    │   ├── bulma-slider.min.css
    │   ├── fontawesome.all.min.css
    │   └── index.css
    └── js/                # JavaScript files
        ├── bulma-carousel.min.js
        ├── bulma-slider.min.js
        ├── fontawesome.all.min.js
        └── index.js
```

## 🚀 Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/signofthefour/pruntts.git
   cd pruntts
   ```

2. **Open the demo**

   ```bash
   # Option 1: Open directly in browser
   open index.html
   
   # Option 2: Serve with Python
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

3. **Explore the demos**

   - Navigate through the audio comparisons
   - Use the interactive controls to compare models
   - Review the methodology images and key results

## 📊 Technical Highlights

### Efficiency Improvements

- **Model Compression**: Systematic layer pruning reduces model depth by 50%
- **Knowledge Distillation**: Preserves semantic fidelity during compression
- **Resource Optimization**: 20% reduction in VRAM usage
- **Data Efficiency**: Requires less than 5% of original training data

### Audio Quality Preservation

- Maintains near-parity with full LLaSA model
- Zero-shot synthesis capabilities retained
- Cross-speaker generalization preserved
- Controllability and prosody modeling maintained

## 🎓 Citation

```bibtex
@article{nguyen2024pruntts,
  title={Prun-TTS: Let Speak with Fewer but Essential Layers},
  author={Nguyen, Tan Dat and Kim, Ji-Hoon and Kim, Jaehun and Chung, Joon Son},
  journal={arXiv preprint arXiv:XXXX.XXXXX},
  year={2024}
}
```

## 📝 License

This website is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

## 🔗 Links

- **Lab Website**: [Multimodal AI Lab - KAIST](https://mm.kaist.ac.kr/)
- **More Research**: [MMAI Publications](https://mmai.io/pubs/)
- **Demo Page**: [Live Demo](index.html)

---

*For questions or collaborations, please contact the corresponding author: [Joon Son Chung](https://mmai.io/joon/)*
