## Services

| service                       | plugin                            | default model                        | port | endpoint             |
|-------------------------------|-----------------------------------|--------------------------------------|------|----------------------|
| HiveMind-core                 | hivemind-websocket-plugin         | `ovos-core `                         | 5678 |                      |
| HiveMind-core                 | hivemind-http-plugin              | `ovos-core`                          | 5679 |                      |
| STT                           | ovos-stt-plugin-fasterwhisper     | `base`                               | 8081 | /stt                 |
| Language Detection<br>(audio) | ovos-stt-plugin-fasterwhisper     | `base`                               | 8081 | /lang_detect         |
| Piper                         | ovos-tts-plugin-piper             | per language<br>(default `alan-low`) | 8082 | /v2/synthesize       |
| Translation                   | ovos-google-translate-plugin      |                                      | 9686 | /translate           |
| Language Detection<br>(text)  | ovos-google-lang-detector-plugin  |                                      | 9686 | /detect              |
| Persona                       | ovos-solver-openai-persona-plugin | llama.json                           | 8337 | /v1/chat/completions |
|                               | ovos-solver-openai-persona-plugin | salamandra.json                      | 8338 | /v1/chat/completions |
|                               | ovos-solver-rivescript-plugin     | rivescript.json                      | 8501 | /v1/chat/completions |
|                               | ovos-solver-aiml-plugin           | aiml.json                            | 8500 | /v1/chat/completions |
|                               | ovos-skill-wolfie                 | wolfram_alpha.json                   | 8401 | /v1/chat/completions |
|                               | ovos-skill-wikipedia              | wikipedia.json                       | 8400 | /v1/chat/completions |
|                               | ovos-skill-ddg                    | ddg.json                             | 8403 | /v1/chat/completions |
|                               | ovos-skill-wordnet                | wordnet.json                         | 8402 | /v1/chat/completions |