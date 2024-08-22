# AI Voice Assistant

This project is an AI-powered voice assistant that converts speech to text, processes the text using a language model, and then converts the output back to speech. The solution leverages several state-of-the-art models and libraries for speech recognition, language processing, and text-to-speech synthesis.

## Overview

<table>
<tr>
<td style="width:70%">
The AI Voice Assistant consists of three main components:
<ul>
<li><strong>Voice-to-Text Conversion</strong>: Converts audio input into text using Whisper, a high-performance speech recognition model.</li>
<li><strong>Text Processing with LLM</strong>: Processes the transcribed text using a Large Language Model (LLaMA) to generate a meaningful response.</li>
<li><strong>Text-to-Speech Conversion</strong>: Converts the processed text back into speech using ParlerTTS, with customizable parameters for voice modulation.</li>
</ul>
</td>
<td style="width:30%">
<img src="https://github.com/user-attachments/assets/80e794f1-6f87-466c-bef7-1ddd5d900200" alt="Flowchart" style="width:100%">
</td>
</tr>
</table>


## Demo


https://github.com/user-attachments/assets/29710db3-f900-4866-af38-16bd8e265bbd


## Libraries and Models Used

### Libraries

- **Wave**: For reading and writing WAV files.
- **WebRTC-VAD**: Implements Voice Activity Detection (VAD).
- **Pydub**: Simplifies audio processing.
- **Faster Whisper**: For high-performance speech-to-text conversion.
- **Transformers**: Library from Hugging Face for working with pre-trained models.
- **Torch**: A deep learning framework for model processing.
- **Parler-TTS**: Converts text to speech with customizable output.

### Models

- **Whisper Model**: Converts audio to text with high accuracy.
- **LLaMA (Large Language Model)**: Processes the transcribed text to generate responses.
- **Parler-TTS**: Synthesizes speech from text, with adjustable voice characteristics.

## Implementation Details

### Voice-to-Text Conversion

- **Audio Format Handling**: Converts input audio to WAV format with a 32kHz sample rate.
- **VAD Filtering**: Filters out non-speech segments to improve transcription accuracy.

### Text Processing with LLM

- **Language Model Usage**: Transcribed text is processed by the LLaMA model to generate relevant responses.
- **Model Tuning**: Adjusts parameters like `top_k`, `top_p`, and `temperature` for optimal text generation.

### Text-to-Speech Conversion

- **Speech Synthesis**: Converts text to speech using Parler-TTS with customizable parameters.
- **VAD Application**: Applies VAD post-synthesis to clean up the output.

## How to Run the Project

1. **Install Required Libraries**:
    ```bash
    pip install webrtcvad pydub faster-whisper transformers torch parler-tts
    ```
2. **Run the Main Script**: 
    - Provide your audio file (either `.m4a` or `.mp3`) to the `transcribe_audio` function.
    - The system will output the transcribed text, the LLM response, and the final synthesized speech.

3. **Check the Output**:
    - The transcribed text, LLM response, and final audio will be printed or saved as needed.

---

Thank you for checking out this project! Feel free to reach out if you have any questions or suggestions.
