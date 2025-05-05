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
![image](https://github.com/user-attachments/assets/c71af1a5-ae1c-45bb-800f-3d5611fefb33)

|                                      | **_Raw Text Quality Metrics_** |         |         |         |          |
|--------------------------------------|:------------------------------:|:-------:|:-------:|:-------:|:--------:|
| **Model**                            |             **WER**            | **CER** | **MER** | **WIL** | **PIER** |
| Whisper Medium                       |                          17,56 |   10,51 |   16,42 |   22,74 |    13,03 |
| Whisper Large-v3-turbo               |                          15,78 |    9,88 |    14,6 |    19,5 |    10,35 |
| Vosk 0,42 RU                         |                          29,78 |   16,96 |    27,5 |   40,19 |    19,61 |
| Seamless-M4T-v2-large                |                          45,73 |    35,4 |   43,79 |   54,78 |    32,14 |
| Wav2Vec-finetuned by Jonatas Grosman |                          54,03 |   25,72 |   49,09 |   69,47 |    41,52 |
| GigaAM (v2_rnnt)                     |                          18,75 |   18,75 |   17,04 |   22,42 |    11,95 |


|                                      | **_Raw Text Quality Metrics_** |         |         |         |          |
|--------------------------------------|:------------------------------:|:-------:|:-------:|:-------:|:--------:|
| **Model**                            |             **WER**            | **CER** | **MER** | **WIL** | **PIER** |
| Whisper Medium                       |                          17,56 |   10,51 |   16,42 |   22,74 |    13,03 |
| Whisper Large-v3-turbo               |                          15,78 |    9,88 |    14,6 |    19,5 |    10,35 |
| Vosk 0,42 RU                         |                          29,78 |   16,96 |    27,5 |   40,19 |    19,61 |
| Seamless-M4T-v2-large                |                          45,73 |    35,4 |   43,79 |   54,78 |    32,14 |
| Wav2Vec-finetuned by Jonatas Grosman |                          54,03 |   25,72 |   49,09 |   69,47 |    41,52 |
| GigaAM (v2_rnnt)                     |                          18,75 |   18,75 |   17,04 |   22,42 |    11,95 |

|                                      |                        |          **_Time Metrics_**         |                                     |         |
|--------------------------------------|------------------------|:-----------------------------------:|:-----------------------------------:|:-------:|
| **Model**                            | **Caclulation Device** |       **Audio Time (seconds)**      | **Time of transcription (seconds)** | **RTF** |
| Whisper Medium                       | CUDA (GPU)             | 40143,3  (~11 hours and 10 minutes) |                              5095,9 |   0,127 |
| Whisper Large-v3-turbo               | CUDA (GPU)             |                                     |                              2309,3 |   0,058 |
| Vosk 0,42 RU                         | CPU                    |                                     |                             11255,6 |    0,28 |
| Seamless-M4T-v2-large                | CUDA (GPU)             |                                     |                               60421 |   1,505 |
| Wav2Vec-finetuned by Jonatas Grosman | CUDA (GPU)             |                                     |                               371,1 |   0,009 |
| GigaAM (v2_rnnt)                     | CUDA (GPU)             |                                     |                              1005,1 |   0,025 |
| Pyannote speaker-diarization-3.1     | CUDA (GPU)             |                                     |                               971,2 |   0,024 |

