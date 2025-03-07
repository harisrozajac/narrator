# David Attenborough narrates your life.

https://twitter.com/charliebholtz/status/1724815159590293764

## Setup

Clone this repo, and setup and activate a virtualenv:

```bash
python3 -m pip install virtualenv
python3 -m virtualenv venv
source venv/bin/activate
```

Then, install the dependencies:
`pip install -r requirements.txt`

You will need ffmpeg to play audio. On Mac, you can install it with `brew install ffmpeg`.

Make a [OpenAI](https://beta.openai.com/), and [ElevenLabs](https://elevenlabs.io) account and set your tokens:

**Open AI API Note**: If you haven't added at least $1 of credit to your OpenAI account, you will not have access to `gpt-4-vision-preview`.

```
export OPENAI_API_KEY=<token>
export ELEVENLABS_API_KEY=<eleven-token>
```

Or use `.env` file and set the variables there.
Make sure to install `python-dotenv` if you want to use this method.
You'll also have to run load_dotenv() in files where you want to use the environment variables.

Make a new voice in Eleven and get the voice id of that voice using their [get voices](https://elevenlabs.io/docs/api-reference/voices) API, or by clicking the flask icon next to the voice in the VoiceLab tab.

```
export ELEVENLABS_VOICE_ID=<voice-id>
```

## Run it!

In a terminal, run the webcam capture:

```bash
python capture.py
```

In another terminal, run the narrator:

```bash
python narrator.py
```
