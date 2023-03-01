SSTV Decoder (modified)
============
Modified version of [SSTV Decoder](https://github.com/colaclanth/sstv)

This version has no console output so it can be used in a bot.


Installation
------------
$ pip install sstv@git+https://github.com/MaximeSharp/sstv.git


Usage
-----
```
from sstv.decode import SSTVDecoder

wav_file = "my_wave_file.wav"
img_file = "my_img_file.png"

with SSTVDecoder(wav_file) as sstv:
  img = sstv.decode(0.0)
  if img is None:
    print("Not a valid audio file")
  try:
    img.save(img_file)
    print("Image saved successfully")
  except:
    print("Error while saving the image")
```

<details>
<summary>Original README.md</summary>

SSTV Decoder
============

![](https://raw.githubusercontent.com/colaclanth/sstv/master/examples/m1.png)

A command line slow-scan television decoder that works on audio files rather than reading a soundcard (like most other decoders).
Currently supports the following modes:
* Martin 1, 2
* Scottie 1, 2, DX
* Robot 36, 72

Installation
------------

```
$ git clone https://github.com/colaclanth/sstv.git

$ python setup.py install
```

Usage
-----

```
$ sstv -d audio_file.wav -o result.png
```

Resources Used
--------------

* SSTV specification/timings - [The Dayton Paper](http://webcache.googleusercontent.com/search?q=cache:GzP65FlYEtwJ:www.barberdsp.com/downloads/Dayton%2520Paper.pdf)
</details>
