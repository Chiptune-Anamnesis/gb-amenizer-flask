# Game Boy Amenizer ROM Sample Replacer

A small Python Flask web app that takes a `.raw` audio sample, applies a 4-bit conversion, and injects it into the first 16 KB of an existing Game Boy ROM (`amenizer.gb`). The result is a new `.gb` file ready to flash to your Game Boy for custom audio samples.

---

## 🚀 Features

- **Web interface**: Upload `.raw` sample files via a simple HTML form.
- **4-bit conversion**: Downsamples each byte to its upper 4 bits.
- **ROM injection**: Overwrites the first 16 KB of `amenizer.gb` with your converted data.
- **File size guard**: Rejects files over 512 KB to prevent excessive uploads.
- **Single-click download**: Returns your customized `.gb` file for immediate use.

---

## 🛠️ Prerequisites

- Python 3.7+
- [pipenv](https://pipenv.pypa.io/en/latest/) or `pip`
- A copy of `amenizer.gb` in the project root
- A `.raw` with no header PCM sample file (8-bit unsigned, mono), 32768 samples long. (32768 Hz), Exactly 1 second loop.

---

## 📖 Getting Started

1. **Clone the repo**  
   ```bash
   git clone https://github.com/Chiptune-Anamnesis/gb-amenizer-replacer.git
   cd gb-amenizer-replacer
   
2. **Install requirements**  
   ```bash
   pip install -r requirements.txt

4. **Set environmental variable**  
   ```bash
   export FLASK_APP=web.py

3. **Run flask app**  
   ```bash
   flask run
   
---

## 🔗 Try the App
- https://crunchypotato.pythonanywhere.com/
   
