# Kokoro TextToSpeech Node for ComfyUI

A custom node for ComfyUI that provides Text-to-Speech capabilities using the Kokoro TTS engine.

## Features

- High-quality text-to-speech synthesis
- Multiple voice options
- Support for multilingual text
- Easy integration with ComfyUI workflows

## Installation

1. Clone this repository into your ComfyUI custom nodes directory:
```bash
cd ComfyUI/custom_nodes
git clone https://github.com/benjiyaya/ComfyUI-KokoroTTS
```

2. Download required model files:
   - Create a folder `Kokorotts` under ComfyUI/models
   - Download the model file and save to 'Kokorotts' folder from: https://huggingface.co/thewh1teagle/kokoro-onnx/resolve/main/kokoro-v0_19.onnx
   - Download the voices file and save to 'Kokorotts' folder from: https://huggingface.co/thewh1teagle/kokoro-onnx/resolve/main/voices.json
   - Place both files in the `ComfyUI/models/Kokorotts` directory

3. Install required Python packages:
```bash
pip install requirements.txt
```

## Available Voices

The following voices are available:
- af (African Female)
- af_sarah (African Female Sarah)
- af_bella (African Female Bella)
- af_nicole (African Female Nicole)
- af_sky (African Female Sky)
- am_adam (African Male Adam)
- am_michael (African Male Michael)
- bf_emma (British Female Emma)
- bf_isabella (British Female Isabella)
- bm_george (British Male George)
- bm_lewis (British Male Lewis)

## Usage

1. In ComfyUI, locate the "Kokoro TextToSpeech" node under the "kokoro" category
2. Connect the node to your workflow
3. Input your text and select a voice
4. The node will output an audio waveform that can be used with other audio nodes

### Input Parameters

- `text`: The text you want to convert to speech (supports multiline text)
- `speaker`: The voice to use for speech synthesis (default: af_sarah)

### Output

- `audio`: Audio data in the format expected by ComfyUI audio nodes

## Error Handling

The node includes comprehensive error handling for common issues:
- Missing model or voice files
- Invalid text input
- TTS generation failures

Error messages will be logged with detailed information to help troubleshoot any issues.

## License

kokoro-onnx: MIT
kokoro model: Apache 2.0

## Credits

- Kokoro TTS Engine: [Include credits for the original Kokoro TTS project]
- ComfyUI: https://github.com/comfyanonymous/ComfyUI
- ComfyUI-BS_Kokoro-onnx https://github.com/Burgstall-labs/ComfyUI-BS_Kokoro-onnx
