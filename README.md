# ASR-Speech-to-Text-Models-Comparison-RU-Language
Here is a pipline to compare open source automatic speech recognition ML models by metrics WER, CER ect.

The following ASR models were tested on my own dataset (10 in-depth interviews: ~11 hours of Russian informal speech):
- OpenAI: [Whisper-large-v3-turbo](https://huggingface.co/openai/whisper-large-v3-turbo)
- OpenAI: [Whisper-medium](https://huggingface.co/openai/whisper-medium)
- Alpha Cephei: [Vosk-model-ru-0.42](https://alphacephei.com/vosk)
- Meta AI: [Seamless-m4t-v2-large](https://huggingface.co/facebook/seamless-m4t-v2-large)
- Meta AI + Jonatas Grosman: [Wav2vec2-large-xlsr-53-russian](https://huggingface.co/jonatasgrosman/wav2vec2-large-xlsr-53-russian)
- Sber Salute Developers: [GigaAM](https://github.com/salute-developers/GigaAM) (ver. v2_rnnt)

Diarization model: 
- Pyannote: [speaker-diarization-3.1](https://huggingface.co/pyannote/speaker-diarization-3.1)

The results:
![image](https://github.com/user-attachments/assets/ce2d0e21-bff6-443b-9632-c7fce946d44b)
						

