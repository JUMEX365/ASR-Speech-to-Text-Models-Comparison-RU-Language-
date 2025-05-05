# ASR-Speech-to-Text-Models-Comparison-RU-Language
Here is a [pipline](https://github.com/JUMEX365/ASR-Speech-to-Text-RU-Models-Comparison/blob/main/ASR_models_comparison_pipeline.ipynb) to compare open source automatic speech recognition ML models by metrics WER, CER ect.

------------------------------------------------------------------------------------------------------------------------

**The following ASR models** were tested on my own dataset (10 in-depth interviews: ~11 hours of Russian informal speech):
- OpenAI: [Whisper-large-v3-turbo](https://huggingface.co/openai/whisper-large-v3-turbo)
- OpenAI: [Whisper-medium](https://huggingface.co/openai/whisper-medium)
- Alpha Cephei: [Vosk-model-ru-0.42](https://alphacephei.com/vosk)
- Meta AI: [Seamless-m4t-v2-large](https://huggingface.co/facebook/seamless-m4t-v2-large)
- Meta AI + Jonatas Grosman: [Wav2vec2-large-xlsr-53-russian](https://huggingface.co/jonatasgrosman/wav2vec2-large-xlsr-53-russian)
- Sber Salute Developers: [GigaAM](https://github.com/salute-developers/GigaAM) (ver. v2_rnnt)

Diarization model: 
- Pyannote: [Speaker-diarization-3.1](https://huggingface.co/pyannote/speaker-diarization-3.1)


## **The results:**

#### _Concise view:_

![image](https://github.com/user-attachments/assets/c71af1a5-ae1c-45bb-800f-3d5611fefb33)

------------------------------------------------------------------------------------------------------------------------

#### _Detailed view:_

|**_Raw Text Quality Metrics_**        |                                |         |         |         |          |
|--------------------------------------|:------------------------------:|:-------:|:-------:|:-------:|:--------:|
| **Model**                            |             **WER**            | **CER** | **MER** | **WIL** | **PIER** |
| Whisper Medium                       |                          17,56 |   10,51 |   16,42 |   22,74 |    13,03 |
| Whisper Large-v3-turbo               |                          15,78 |    9,88 |    14,6 |    19,5 |    10,35 |
| Vosk 0,42 RU                         |                          29,78 |   16,96 |    27,5 |   40,19 |    19,61 |
| Seamless-M4T-v2-large                |                          45,73 |    35,4 |   43,79 |   54,78 |    32,14 |
| Wav2Vec-finetuned by Jonatas Grosman |                          54,03 |   25,72 |   49,09 |   69,47 |    41,52 |
| GigaAM (v2_rnnt)                     |                          18,75 |   18,75 |   17,04 |   22,42 |    11,95 |

------------------------------------------------------------------------------------------------------------------------

|**_Lemmatized Text Quality Metrics_** |                                       |         |         |         |          |
|--------------------------------------|:-------------------------------------:|:-------:|:-------:|:-------:|:--------:|
| **Model**                            |                **WER**                | **CER** | **MER** | **WIL** | **PIER** |
| Whisper Medium                       |                                 16,15 |   10,41 |    15,1 |   20,25 |    12,78 |
| Whisper Large-v3-turbo               |                                 14,64 |    9,79 |    9,79 |   17,46 |    10,25 |
| Vosk 0,42 RU                         |                                  26,9 |   16,73 |   24,82 |   35,58 |    16,83 |
| Seamless-M4T-v2-large                |                                 43,68 |   43,68 |   41,81 |   51,49 |    29,64 |
| Wav2Vec-finetuned by Jonatas Grosman |                                 50,69 |   50,69 |   45,99 |   65,54 |     36,7 |
| GigaAM (v2_rnnt)                     |                                 17,61 |   12,16 |   16,01 |   20,45 |    13,08 |

------------------------------------------------------------------------------------------------------------------------

**Audio Total Length**: 40143,3 seconds (or ~11 hours and 10 minutes)

|**_Time Metrics_**                    |                        | _(seconds)_                         |         | 
|--------------------------------------|------------------------|:-----------------------------------:|:-------:|
| **Model**                            | **Caclulation Device** | **Time of work**                    | **RTF** |
| Whisper Medium                       | CUDA (GPU)             |                              5095,9 |   0,127 |
| Whisper Large-v3-turbo               | CUDA (GPU)             |                              2309,3 |   0,058 |
| Vosk 0,42 RU                         | CPU                    |                             11255,6 |    0,28 |
| Seamless-M4T-v2-large                | CUDA (GPU)             |                               60421 |   1,505 |
| Wav2Vec-finetuned by Jonatas Grosman | CUDA (GPU)             |                               371,1 |   0,009 |
| GigaAM (v2_rnnt)                     | CUDA (GPU)             |                              1005,1 |   0,025 |
| Pyannote speaker-diarization-3.1     | CUDA (GPU)             |                               971,2 |   0,024 |

------------------------------------------------------------------------------------------------------------------------

## Clarifications:
* More info about metrics: [Morris, Andrew & Maier, Viktoria & Green, Phil. (2004). From WER and RIL to MER and WIL: improved evaluation measures for connected speech recognition. 10.21437/Interspeech.2004-668.](https://www.researchgate.net/publication/221478089_From_WER_and_RIL_to_MER_and_WIL_improved_evaluation_measures_for_connected_speech_recognition)
* _PIER_ is custom metric that means _Position Independent Word Error Rate_
* Actual date of presented results ~ April 2025
