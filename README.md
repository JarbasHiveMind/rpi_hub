```bash
#!/bin/bash
echo -e "\e[1;34m
                  ===  @              @  ######@@@@@@@@#%     ##         #   ===
                 ===    @ @           @%########% @%#@@@@@@@     ##%    %#    ===
                ===      @         @@@@%########% #   @@@@@@@@@@   %#    #  %  ===
               ===      @ @@@@@@@@@@@@@@@######% %#   %  @@@@@@@@%@#%    %     %====
              ===  @@@@@@@@@@@@@@@@@@@@          ## %       @@%@@@@#@@   %       +==+
             ===        @ @@@@@@@@@  @           #%            @@@@#@@@@@  %@      ===
            ===        @@@@@@@@@    @            %%                #@@@@@@@@  @#%@  ===
           === @   @@@@@@@@@@  @   @             ##               ##  @@@@@@@@@      ===
          ==+     @@@@@@@@          @               ##%        ##        @@@@@@@@     ===
         ==+      @@@@@            @   @      @@@@@@@  ### ### ######       @@@@@      ===
       +==+       @@@@@                @     @@@@@@@@@      ############    @@@@@       ===
      +==         @@@@                     @@@@@@@@@@@@   ################  @@@@@        ===
     +==          @@@@   @          @       @@@@@@@@@@@   ################  @@@@@         ===
    +==           @@@@    @        @         @@@@@@@@@    ################  @@@@@          +==
   ===            @@@@                        @@@@@@@     ################  @@@@@           ===+
  ===             @@@---------------------------------------------------------@@@            ===+
 ===   %##%##     @@@-@#--@--@@@-+@--#@--@@@------@@---@@--@@@--@@--@---@@@+--@@@   @         ====
===   ########%   @@@-@#==@---@---@*-@---@==------@@@-@*@---@---@@@-@---@--@@-@@@    @         +===
+==+ ###########  @@@-@#--@---@----@@@---@--------@@@+@*@---@---@-%@@---@--@@-@@@     @        ===+
 +==*###########% @@@-@*--@--@@@---#@----@@@------%%-@-+@--@@@--@--*@---@@%---@@@      @@@@@@@===
  ===+##########  @@@---------------------------------------------------------@@@            ===
   +===########  ###########%#                 #  ###########               @@@@@           ===
     ===######  ################%##%%##       #      ####%                  @@@@@@@@@@@    ===
      ===      ############### #             #                              @@@@@       @+===
       ===    ################# #           #@                        @     @@@@@       +===
        ===    ###############%  ###########%                         @     @@@@@      ====
         ===    #############%             @                           @    @@@@@     ====
          ===    ###########%               %                           @ @@@@@@@    ====
           ===    #########%          ##%%#####                       @@@@@@@@@     ====
            ===       @@@@@@@@@      #     #   #                   @@@@@@@@@       ====
             ===         @@@@@@@@@  #     #     %               @@@@@@@@@         ===+
              ===           @@@@@@@%@    %       %           @@@@@@@@@           ===+
               ===+             @@@#@@@@@      ########   @@@@@@@@@             ===
                +==+               @#@@@@@@@  #  #     %@@@@@@@@               ===
                  ===                %@@@@@@@#@ #  @@@@@#@@@@                 ===
                   ===                %  @@@%@@%@@@@@@@@@#                   ===

                                 ==============================
                                 --- Welcome to HiveMind Hub ---
                                     Rpi5 Development Edition    
                                 ==============================

\e[0m"
```

## Services

| service                       | plugin                                                                                        | default model                        | port | endpoint             |
|-------------------------------|-----------------------------------------------------------------------------------------------|--------------------------------------|------|----------------------|
| HiveMind-core                 | hivemind-websocket-plugin                                                                     | `ovos-core `                         | 5678 |                      |
|                               | hivemind-http-plugin                                                                          | `ovos-core`                          | 5679 |                      |
| STT                           | ovos-stt-plugin-chromium                                                                      | google proxy                         | 8085 | /stt                 |
|                               | ovos-stt-plugin-fasterwhisper                                                                 | `tiny`                               | 8081 | /stt                 |
| Language Detection<br>(audio) | ovos-stt-plugin-fasterwhisper                                                                 | `tiny`                               | 8081 | /lang_detect         |
| TTS                           | ovos-tts-plugin-google-tx                                                                     | google proxy                         | 8090 | /v2/synthesize       |
|                               | ovos-tts-plugin-piper                                                                         | per language<br>(default `alan-low`) | 8082 | /v2/synthesize       |
| Translation                   | ovos-google-translate-plugin                                                                  | google proxy                         | 9686 | /translate           |
| Language Detection<br>(text)  | ovos-google-lang-detector-plugin                                                              | google proxy                         | 9686 | /detect              |
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

### Timings

rpi5 8GB
____

**whisper tiny** ~25 seconds (`lang: auto`)

```bash
2025-01-29 02:00:52.904 - voice - ovos_stt_plugin_server:execute:114 - DEBUG - chosen url http://0.0.0.0:8081/stt
2025-01-29 02:01:18.573 - voice - ovos_dinkum_listener.voice_loop.voice_loop:_after_cmd:789 - INFO - Raw transcription: [('Tell me a joke.', 1.0)]
```

**tiny llama** ~1 minute 30 seconds (first sentence) / ~10 seconds (follow up sentences)

```bash
2025-01-29 02:10:26.629 - skills - ovos_core.intent_services:handle_utterance:416 - INFO - fallback_medium match: PipelineMatch(match_type=True, match_data={}, skill_id='skill-ovos-fallback-chatgpt.openvoiceos', utterance='Explain Quantum Mechanics', updated_session=None, handled=True)
2025-01-29 02:11:43.992 - audio - ovos_audio.service:execute_tts:415 - INFO - Speak:  It is a branch of classical mechanics that is based on the principles of quantum theory, which is a branch of theoretical physics that describes the behavior of subatomic particles.
2025-01-29 02:11:53.534 - audio - ovos_audio.service:execute_tts:415 - INFO - Speak: Quantum mechanics is based on the idea that particles have both wave and particle properties.
2025-01-29 02:12:08.781 - audio - ovos_audio.service:execute_tts:415 - INFO - Speak:  This means that particles can be described as both waves and particles, and that their behavior is governed by the laws of physics that apply to waves.
```
