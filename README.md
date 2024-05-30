<div align="center">

# Insta360_MaterialOrganization

[**English**](./README.md) | [**中文简体**](./README_zh_CN.md)

[![Licence](https://img.shields.io/badge/LICENSE-GPL3.0-green.svg?style=for-the-badge)](https://github.com/Han-Zhong/Insta360_MaterialOrganization/blob/main/LICENSE)

For Organizing All "Insta360 Pro 2" and "Insta360 Titan" SD Card Materials
will update description soon!

</div>

## Usage

### Inference

#### GUI

![GUI](https://raw.githubusercontent.com/voicepaw/so-vits-svc-fork/main/docs/_static/gui.png)

GUI launches with the following command:

```shell
svcg
```

#### CLI

- Realtime (from microphone)

```shell
svc vc
```

- File

```shell
svc infer source.wav
```

Pretrained models are available on [Hugging Face](https://huggingface.co/models?search=so-vits-svc) or [CIVITAI](https://civitai.com/?query=so-vits-svc).

#### Notes

- If using WSL, please note that WSL requires additional setup to handle audio and the GUI will not work without finding an audio device.
- In real-time inference, if there is noise on the inputs, the HuBERT model will react to those as well. Consider using realtime noise reduction applications such as [RTX Voice](https://www.nvidia.com/en-us/geforce/guides/nvidia-rtx-voice-setup-guide/) in this case.
- Models other than for 4.0v1 or this repository are not supported.
- GPU inference requires at least 4 GB of VRAM. If it does not work, try CPU inference as it is fast enough. [^r-inference]

[^r-inference]: [#469](https://github.com/voicepaw/so-vits-svc-fork/issues/469)

### Training

#### Before training

- If your dataset has BGM, please remove the BGM using software such as [Ultimate Vocal Remover](https://ultimatevocalremover.com/). `3_HP-Vocal-UVR.pth` or `UVR-MDX-NET Main` is recommended. [^1]
- If your dataset is a long audio file with a single speaker, use `svc pre-split` to split the dataset into multiple files (using `librosa`).
- If your dataset is a long audio file with multiple speakers, use `svc pre-sd` to split the dataset into multiple files (using `pyannote.audio`). Further manual classification may be necessary due to accuracy issues. If speakers speak with a variety of speech styles, set --min-speakers larger than the actual number of speakers. Due to unresolved dependencies, please install `pyannote.audio` manually: `pip install pyannote-audio`.
- To manually classify audio files, `svc pre-classify` is available. Up and down arrow keys can be used to change the playback speed.