```mermaid
flowchart TD
    boil[boilerplate
    finished 2025_04_12]
    welcome[welcome page in vue]
    dash[dashboard menu in vue]
    prompts[marketing data AI prompts in python or golang]
    save[data save logic]
    clips[python video clip editing]
    data[marketing data page in vue]
    schedule[AI generated marketing campaign schedule page]
    message[AI generated video message editing page]
    result[compiled video review page]
    boil --> welcome
    welcome --> dash
    dash --> prompts
    dash --> data
    prompts --> data
    schedule --> save
    save --> message
    data --> schedule
    schedule --> message
    message --> clips
    clips --> result
    message --> result

```