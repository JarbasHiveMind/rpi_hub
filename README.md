## Services

| service                       | plugin                                                                                        | default model                        | port | endpoint             |
|-------------------------------|-----------------------------------------------------------------------------------------------|--------------------------------------|------|----------------------|
| HiveMind-core                 | hivemind-websocket-plugin                                                                     | `ovos-core `                         | 5678 |                      |
| HiveMind-core                 | hivemind-http-plugin                                                                          | `ovos-core`                          | 5679 |                      |
| STT                           | ovos-stt-plugin-fasterwhisper                                                                 | `tiny`                               | 8081 | /stt                 |
| Language Detection<br>(audio) | ovos-stt-plugin-fasterwhisper                                                                 | `tiny`                               | 8081 | /lang_detect         |
| Piper                         | ovos-tts-plugin-piper                                                                         | per language<br>(default `alan-low`) | 8082 | /v2/synthesize       |
| Translation                   | ovos-google-translate-plugin                                                                  |                                      | 9686 | /translate           |
| Language Detection<br>(text)  | ovos-google-lang-detector-plugin                                                              |                                      | 9686 | /detect              |
| Persona                       | [ovos-solver-gguf-plugin](https://github.com/TigreGotico/ovos-solver-gguf-plugin)             | tinyllama.json                       | 8337 | /v1/chat/completions |
|                               | [ovos-solver-rivescript-plugin](https://github.com/OpenVoiceOS/ovos-solver-plugin-rivescript) | rivescript.json                      | 8501 | /v1/chat/completions |
|                               | [ovos-solver-aiml-plugin](https://github.com/OpenVoiceOS/ovos-solver-plugin-aiml)             | aiml.json                            | 8500 | /v1/chat/completions |
|                               | [ovos-skill-wolfie](https://github.com/OpenVoiceOS/ovos-skill-wolfie)                         | wolfram_alpha.json                   | 8401 | /v1/chat/completions |
|                               | [ovos-skill-wikipedia](https://github.com/OpenVoiceOS/ovos-skill-wikipedia)                   | wikipedia.json                       | 8400 | /v1/chat/completions |
|                               | [ovos-skill-ddg](https://github.com/OpenVoiceOS/ovos-skill-ddg)                               | ddg.json                             | 8403 | /v1/chat/completions |
|                               | [ovos-skill-wordnet](https://github.com/OpenVoiceOS/ovos-skill-wordnet)                       | wordnet.json                         | 8402 | /v1/chat/completions |
|                               | [g4f](https://github.com/xtekky/gpt4free)                                                     | https://duckduckgo.com/aichat        | 1337 | /v1/chat/completions |
| Image Generation              | [g4f](https://github.com/xtekky/gpt4free)                                                     |                                      | 1337 | /v1/images/generate  |

### OVOS Plugins

OVOS plugins integrate with OpenVoiceOS via mycroft.conf and also double as client libraries

- STT:
    - [ovos-stt-plugin-server](https://github.com/OpenVoiceOS/ovos-stt-server-plugin)
- TTS:
    - [ovos-tts-plugin-server](https://github.com/OpenVoiceOS/ovos-tts-server-plugin)
- Translation:
    - [ovos-translate-server-plugin](https://github.com/OpenVoiceOS/ovos-translate-server-plugin)
- persona (OpenAI compatible):
    - [ovos-skill-fallback-chatgpt](https://github.com/OpenVoiceOS/ovos-skill-fallback-chatgpt)
    - [ovos-solver-openai-persona-plugin](https://github.com/OpenVoiceOS/ovos-solver-openai-persona-plugin)
