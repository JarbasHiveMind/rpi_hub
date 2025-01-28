## Services

| service                       | plugin                                            | model                                | port | endpoint             |
|-------------------------------|---------------------------------------------------|--------------------------------------|------|----------------------|
| HiveMind-core                 | hivemind-websocket-plugin                         | `ovos-core `                         | 5678 |                      |
| HiveMind-core                 | hivemind-http-plugin                              | `ovos-core`                          | 5679 |                      |
| STT                           | ovos-stt-plugin-fasterwhisper                     | `base`                               | 8081 | /stt                 |
| Language Detection<br>(audio) | ovos-stt-plugin-fasterwhisper                     | `base`                               | 8081 | /lang_detect         |
| Piper                         | ovos-tts-plugin-piper                             | per language<br>(default `alan-low`) | 8082 | /v2/synthesize       |
| Persona                       | ovos-solver-openai-persona-plugin                 | https://llama.smartgic.io            | 8337 | /v1/chat/completions |
| Translation                   | ovos-google-translate-plugin                      |                                      | 9686 | /translate           |
| Language Detection<br>(text)  | ovos-google-lang-detector-plugin                  |                                      | 9686 | /detect              |