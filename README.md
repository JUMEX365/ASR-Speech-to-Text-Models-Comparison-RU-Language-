# ASR-Speech-to-Text-Models-Comparison-RU-Language
Here is a pipline to compare open source automatic speech recognition ML models by metrics WER, CER ect.

The following models were tested on my own dataset (10 in-depth interviews: ~11 hours of Russian informal speech):
- whisper-large-v3-turbo (https://huggingface.co/openai/whisper-large-v3-turbo)
- whisper-medium (https://huggingface.co/openai/whisper-medium)
- vosk-model-ru-0.42 (https://alphacephei.com/vosk)
- seamless-m4t-v2-large (https://huggingface.co/facebook/seamless-m4t-v2-large)
- wav2vec2-large-xlsr-53-russian (https://huggingface.co/jonatasgrosman/wav2vec2-large-xlsr-53-russian)
- GigaAM (ver. v2_rnnt) (https://github.com/salute-developers/GigaAM) 

The results:
		Time Metrics			Raw Text Quality Metrics					Lemmatized Text Quality Metrics				
Model	Caclulation Device 	Audio Time (seconds)	Time of transcribation (seconds)	RTF	WER	CER	MER	WIL	PIER	WER	CER	MER	WIL	PIER
Generalized 10 sample														
Whisper Medium	CUDA (GPU)	"40143,3

(~11 hours and 10 minutes)"	5095,9	0,127	17,56	10,51	16,42	22,74	13,03	16,15	10,41	15,1	20,25	12,78
Whisper Large-v3-turbo	CUDA (GPU)		2309,3	0,058	15,78	9,88	14,6	19,5	10,35	14,64	9,79	9,79	17,46	10,25
Vosk 0,42 RU	CPU		11255,6	0,28	29,78	16,96	27,5	40,19	19,61	26,9	16,73	24,82	35,58	16,83
Seamless-M4T-v2-large	CUDA (GPU)		60421	1,505	45,73	35,4	43,79	54,78	32,14	43,68	43,68	41,81	51,49	29,64
Wav2Vec-finetuned by jonatasgrosman	CUDA (GPU)		371,1	0,009	54,03	25,72	49,09	69,47	41,52	50,69	50,69	45,99	65,54	36,7
GigaAM (v2_rnnt)	CUDA (GPU)		1005,1	0,025	18,75	18,75	17,04	22,42	11,95	17,61	12,16	16,01	20,45	13,08
pyannote/speaker-diarization-3.1	CUDA (GPU)		971,2	0,024										

