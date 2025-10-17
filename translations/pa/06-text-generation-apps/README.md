<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "00e33cd3ff945511446ecda4a9f8a828",
  "translation_date": "2025-10-17T14:19:46+00:00",
  "source_file": "06-text-generation-apps/README.md",
  "language_code": "pa"
}
-->
# ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪਲੀਕੇਸ਼ਨ ਬਣਾਉਣਾ

[![ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪਲੀਕੇਸ਼ਨ ਬਣਾਉਣਾ](../../../translated_images/06-lesson-banner.a5c629f990a636c852353c5533f1a6a218ece579005e91f96339d508d9cf8f47.pa.png)](https://youtu.be/0Y5Luf5sRQA?si=t_xVg0clnAI4oUFZ)

> _(ਉਪਰ ਦਿੱਤੀ ਤਸਵੀਰ 'ਤੇ ਕਲਿਕ ਕਰਕੇ ਇਸ ਪਾਠ ਦਾ ਵੀਡੀਓ ਵੇਖੋ)_

ਤੁਹਾਨੂੰ ਇਸ ਕੋਰਸ ਵਿੱਚ ਹੁਣ ਤੱਕ ਦੇਖਣ ਨੂੰ ਮਿਲਿਆ ਹੈ ਕਿ ਕੁਝ ਮੁੱਖ ਧਾਰਨਾਵਾਂ ਹਨ ਜਿਵੇਂ ਕਿ ਪ੍ਰੌਮਪਟਸ ਅਤੇ ਇੱਕ ਪੂਰੀ ਵਿਧਾ "ਪ੍ਰੌਮਪਟ ਇੰਜੀਨੀਅਰਿੰਗ" ਕਹੀ ਜਾਂਦੀ ਹੈ। ਕਈ ਟੂਲ ਜਿਵੇਂ ChatGPT, Office 365, Microsoft Power Platform ਅਤੇ ਹੋਰ ਤੁਹਾਨੂੰ ਪ੍ਰੌਮਪਟਸ ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਕੁਝ ਹਾਸਲ ਕਰਨ ਵਿੱਚ ਸਹਾਇਤਾ ਕਰਦੇ ਹਨ।

ਜੇ ਤੁਸੀਂ ਆਪਣੇ ਐਪ ਵਿੱਚ ਇਸ ਤਰ੍ਹਾਂ ਦਾ ਅਨੁਭਵ ਸ਼ਾਮਲ ਕਰਨਾ ਚਾਹੁੰਦੇ ਹੋ, ਤਾਂ ਤੁਹਾਨੂੰ ਪ੍ਰੌਮਪਟਸ, ਕੰਪਲੀਸ਼ਨਸ ਅਤੇ ਇੱਕ ਲਾਇਬ੍ਰੇਰੀ ਚੁਣਨ ਵਰਗੀਆਂ ਧਾਰਨਾਵਾਂ ਨੂੰ ਸਮਝਣ ਦੀ ਲੋੜ ਹੈ। ਇਹੀ ਕੁਝ ਤੁਸੀਂ ਇਸ ਅਧਿਆਇ ਵਿੱਚ ਸਿੱਖੋਗੇ।

## ਪਰਿਚਯ

ਇਸ ਅਧਿਆਇ ਵਿੱਚ, ਤੁਸੀਂ:

- openai ਲਾਇਬ੍ਰੇਰੀ ਅਤੇ ਇਸ ਦੀਆਂ ਮੁੱਖ ਧਾਰਨਾਵਾਂ ਬਾਰੇ ਸਿੱਖੋਗੇ।
- openai ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਇੱਕ ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਬਣਾਉਣਗੇ।
- ਪ੍ਰੌਮਪਟ, ਟੈਂਪਰੇਚਰ ਅਤੇ ਟੋਕਨ ਵਰਗੀਆਂ ਧਾਰਨਾਵਾਂ ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਇੱਕ ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਬਣਾਉਣ ਦਾ ਤਰੀਕਾ ਸਮਝੋਗੇ।

## ਸਿੱਖਣ ਦੇ ਲਕਸ਼

ਇਸ ਪਾਠ ਦੇ ਅੰਤ ਵਿੱਚ, ਤੁਸੀਂ ਇਹ ਸਮਝ ਸਕੋਗੇ:

- ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਕੀ ਹੈ, ਇਹ ਸਮਝਾਉਣਾ।
- openai ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਇੱਕ ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਬਣਾਉਣਾ।
- ਆਪਣੇ ਐਪ ਨੂੰ ਵੱਧ ਜਾਂ ਘੱਟ ਟੋਕਨ ਵਰਤਣ ਲਈ ਅਤੇ ਨਤੀਜੇ ਵਿੱਚ ਵੱਖ-ਵੱਖਤਾ ਲਿਆਉਣ ਲਈ ਟੈਂਪਰੇਚਰ ਬਦਲਣ ਲਈ ਕਨਫਿਗਰ ਕਰਨਾ।

## ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਕੀ ਹੈ?

ਆਮ ਤੌਰ 'ਤੇ ਜਦੋਂ ਤੁਸੀਂ ਇੱਕ ਐਪ ਬਣਾਉਂਦੇ ਹੋ, ਤਾਂ ਇਸ ਵਿੱਚ ਹੇਠਾਂ ਦਿੱਤੇ ਤਰੀਕਿਆਂ ਵਿੱਚੋਂ ਕੋਈ ਇੱਕ ਇੰਟਰਫੇਸ ਹੁੰਦਾ ਹੈ:

- ਕਮਾਂਡ-ਅਧਾਰਿਤ। ਕਮਾਂਡ-ਲਾਈਨ ਐਪਸ ਆਮ ਤੌਰ 'ਤੇ ਉਹ ਐਪ ਹੁੰਦੇ ਹਨ ਜਿੱਥੇ ਤੁਸੀਂ ਇੱਕ ਕਮਾਂਡ ਟਾਈਪ ਕਰਦੇ ਹੋ ਅਤੇ ਇਹ ਇੱਕ ਕੰਮ ਕਰਦਾ ਹੈ। ਉਦਾਹਰਣ ਲਈ, `git` ਇੱਕ ਕਮਾਂਡ-ਅਧਾਰਿਤ ਐਪ ਹੈ।
- ਯੂਜ਼ਰ ਇੰਟਰਫੇਸ (UI)। ਕੁਝ ਐਪਸ ਵਿੱਚ ਗ੍ਰਾਫਿਕਲ ਯੂਜ਼ਰ ਇੰਟਰਫੇਸ (GUIs) ਹੁੰਦੇ ਹਨ ਜਿੱਥੇ ਤੁਸੀਂ ਬਟਨ ਕਲਿਕ ਕਰਦੇ ਹੋ, ਟੈਕਸਟ ਦਾਖਲ ਕਰਦੇ ਹੋ, ਵਿਕਲਪ ਚੁਣਦੇ ਹੋ ਅਤੇ ਹੋਰ ਕੁਝ ਕਰਦੇ ਹੋ।

### ਕਮਾਂਡ ਅਤੇ UI ਐਪਸ ਦੀਆਂ ਸੀਮਾਵਾਂ

ਇਸਨੂੰ ਇੱਕ ਕਮਾਂਡ-ਅਧਾਰਿਤ ਐਪ ਨਾਲ ਤੁਲਨਾ ਕਰੋ ਜਿੱਥੇ ਤੁਸੀਂ ਇੱਕ ਕਮਾਂਡ ਟਾਈਪ ਕਰਦੇ ਹੋ:

- **ਇਹ ਸੀਮਿਤ ਹੈ**। ਤੁਸੀਂ ਕੋਈ ਵੀ ਕਮਾਂਡ ਟਾਈਪ ਨਹੀਂ ਕਰ ਸਕਦੇ, ਸਿਰਫ ਉਹ ਜੋ ਐਪ ਸਹਾਇਕ ਹੈ।
- **ਭਾਸ਼ਾ-ਵਿਸ਼ੇਸ਼**। ਕੁਝ ਐਪਸ ਕਈ ਭਾਸ਼ਾਵਾਂ ਦਾ ਸਮਰਥਨ ਕਰਦੇ ਹਨ, ਪਰ ਡਿਫਾਲਟ ਤੌਰ 'ਤੇ ਐਪ ਇੱਕ ਵਿਸ਼ੇਸ਼ ਭਾਸ਼ਾ ਲਈ ਬਣਾਇਆ ਜਾਂਦਾ ਹੈ, ਭਾਵੇਂ ਤੁਸੀਂ ਹੋਰ ਭਾਸ਼ਾਵਾਂ ਦਾ ਸਮਰਥਨ ਸ਼ਾਮਲ ਕਰ ਸਕਦੇ ਹੋ।

### ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪਸ ਦੇ ਫਾਇਦੇ

ਤਾਂ ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਕਿਵੇਂ ਵੱਖਰਾ ਹੈ?

ਇੱਕ ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਵਿੱਚ, ਤੁਹਾਡੇ ਕੋਲ ਵੱਧ ਲਚੀਲਾਪਨ ਹੁੰਦਾ ਹੈ, ਤੁਸੀਂ ਸਿਰਫ ਕੁਝ ਕਮਾਂਡਸ ਜਾਂ ਇੱਕ ਵਿਸ਼ੇਸ਼ ਇਨਪੁਟ ਭਾਸ਼ਾ ਤੱਕ ਸੀਮਿਤ ਨਹੀਂ ਹੁੰਦੇ। ਇਸ ਦੀ ਬਜਾਏ, ਤੁਸੀਂ ਐਪ ਨਾਲ ਸੰਚਾਰ ਕਰਨ ਲਈ ਕੁਦਰਤੀ ਭਾਸ਼ਾ ਦੀ ਵਰਤੋਂ ਕਰ ਸਕਦੇ ਹੋ। ਇੱਕ ਹੋਰ ਫਾਇਦਾ ਇਹ ਹੈ ਕਿ ਤੁਸੀਂ ਪਹਿਲਾਂ ਹੀ ਇੱਕ ਡਾਟਾ ਸਰੋਤ ਨਾਲ ਸੰਚਾਰ ਕਰ ਰਹੇ ਹੋ ਜੋ ਬਹੁਤ ਵੱਡੇ ਜਾਣਕਾਰੀ ਦੇ ਸੰਗ੍ਰਹਿ 'ਤੇ ਪ੍ਰਸ਼ਿਕਸ਼ਿਤ ਕੀਤਾ ਗਿਆ ਹੈ, ਜਦਕਿ ਇੱਕ ਰਵਾਇਤੀ ਐਪ ਡਾਟਾਬੇਸ ਵਿੱਚ ਮੌਜੂਦ ਜਾਣਕਾਰੀ ਤੱਕ ਸੀਮਿਤ ਹੋ ਸਕਦਾ ਹੈ।

### ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਨਾਲ ਕੀ ਬਣਾਇਆ ਜਾ ਸਕਦਾ ਹੈ?

ਤੁਸੀਂ ਕਈ ਚੀਜ਼ਾਂ ਬਣਾਉਣ ਲਈ ਇਸ ਦੀ ਵਰਤੋਂ ਕਰ ਸਕਦੇ ਹੋ। ਉਦਾਹਰਣ ਲਈ:

- **ਚੈਟਬੋਟ**। ਇੱਕ ਚੈਟਬੋਟ ਜੋ ਵਿਸ਼ਿਆਂ ਬਾਰੇ ਸਵਾਲਾਂ ਦੇ ਜਵਾਬ ਦਿੰਦਾ ਹੈ, ਜਿਵੇਂ ਕਿ ਤੁਹਾਡੀ ਕੰਪਨੀ ਅਤੇ ਇਸ ਦੇ ਉਤਪਾਦ।
- **ਮਦਦਗਾਰ**। LLMs ਟੈਕਸਟ ਨੂੰ ਸੰਖੇਪ ਕਰਨ, ਟੈਕਸਟ ਤੋਂ ਅੰਤਰਦ੍ਰਿਸ਼ਟੀ ਪ੍ਰਾਪਤ ਕਰਨ, ਰਿਜ਼ੂਮ ਵਰਗਾ ਟੈਕਸਟ ਤਿਆਰ ਕਰਨ ਵਿੱਚ ਬਹੁਤ ਵਧੀਆ ਹਨ।
- **ਕੋਡ ਸਹਾਇਕ**। ਮਾਡਲ ਦੇ ਅਧਾਰ 'ਤੇ, ਤੁਸੀਂ ਇੱਕ ਕੋਡ ਸਹਾਇਕ ਬਣਾਉਣ ਲਈ ਵਰਤ ਸਕਦੇ ਹੋ ਜੋ ਤੁਹਾਨੂੰ ਕੋਡ ਲਿਖਣ ਵਿੱਚ ਮਦਦ ਕਰਦਾ ਹੈ। ਉਦਾਹਰਣ ਲਈ, ਤੁਸੀਂ GitHub Copilot ਜਾਂ ChatGPT ਵਰਗੇ ਉਤਪਾਦ ਦੀ ਵਰਤੋਂ ਕਰ ਸਕਦੇ ਹੋ।

## ਸ਼ੁਰੂਆਤ ਕਿਵੇਂ ਕਰੀਏ?

ਤੁਹਾਨੂੰ ਇੱਕ LLM ਨਾਲ ਇੰਟੀਗਰੇਟ ਕਰਨ ਦਾ ਤਰੀਕਾ ਲੱਭਣਾ ਪਵੇਗਾ, ਜੋ ਆਮ ਤੌਰ 'ਤੇ ਹੇਠਾਂ ਦਿੱਤੇ ਦੋ ਤਰੀਕਿਆਂ ਵਿੱਚੋਂ ਇੱਕ ਨੂੰ ਸ਼ਾਮਲ ਕਰਦਾ ਹੈ:

- API ਦੀ ਵਰਤੋਂ ਕਰੋ। ਇੱਥੇ ਤੁਸੀਂ ਆਪਣੇ ਪ੍ਰੌਮਪਟ ਨਾਲ ਵੈੱਬ ਰਿਕਵੈਸਟ ਬਣਾਉਂਦੇ ਹੋ ਅਤੇ ਵਾਪਸ ਜਨਰੇਟ ਕੀਤਾ ਟੈਕਸਟ ਪ੍ਰਾਪਤ ਕਰਦੇ ਹੋ।
- ਲਾਇਬ੍ਰੇਰੀ ਦੀ ਵਰਤੋਂ ਕਰੋ। ਲਾਇਬ੍ਰੇਰੀਆਂ API ਕਾਲਾਂ ਨੂੰ ਸਧਾਰਨ ਬਣਾਉਂਦੀਆਂ ਹਨ ਅਤੇ ਵਰਤਣ ਵਿੱਚ ਆਸਾਨ ਬਣਾਉਂਦੀਆਂ ਹਨ।

## ਲਾਇਬ੍ਰੇਰੀ/SDKs

LLMs ਨਾਲ ਕੰਮ ਕਰਨ ਲਈ ਕੁਝ ਜਾਣੇ-ਪਛਾਣੇ ਲਾਇਬ੍ਰੇਰੀ ਹਨ ਜਿਵੇਂ:

- **openai**, ਇਹ ਲਾਇਬ੍ਰੇਰੀ ਤੁਹਾਡੇ ਮਾਡਲ ਨਾਲ ਜੁੜਨ ਅਤੇ ਪ੍ਰੌਮਪਟ ਭੇਜਣ ਨੂੰ ਆਸਾਨ ਬਣਾਉਂਦੀ ਹੈ।

ਫਿਰ ਕੁਝ ਉੱਚ ਪੱਧਰ ਦੀਆਂ ਲਾਇਬ੍ਰੇਰੀਆਂ ਹਨ ਜਿਵੇਂ:

- **Langchain**। Langchain ਜਾਣੀ-ਪਛਾਣੀ ਹੈ ਅਤੇ Python ਦਾ ਸਮਰਥਨ ਕਰਦੀ ਹੈ।
- **Semantic Kernel**। Semantic Kernel Microsoft ਦੀ ਲਾਇਬ੍ਰੇਰੀ ਹੈ ਜੋ C#, Python, ਅਤੇ Java ਭਾਸ਼ਾਵਾਂ ਦਾ ਸਮਰਥਨ ਕਰਦੀ ਹੈ।

## ਪਹਿਲਾ ਐਪ openai ਦੀ ਵਰਤੋਂ ਕਰਕੇ

ਆਓ ਵੇਖੀਏ ਕਿ ਅਸੀਂ ਆਪਣਾ ਪਹਿਲਾ ਐਪ ਕਿਵੇਂ ਬਣਾਉਂਦੇ ਹਾਂ, ਕੀ ਲਾਇਬ੍ਰੇਰੀਆਂ ਦੀ ਲੋੜ ਹੈ, ਅਤੇ ਹੋਰ।

### openai ਇੰਸਟਾਲ ਕਰੋ

OpenAI ਜਾਂ Azure OpenAI ਨਾਲ ਸੰਚਾਰ ਕਰਨ ਲਈ ਬਹੁਤ ਸਾਰੀਆਂ ਲਾਇਬ੍ਰੇਰੀਆਂ ਉਪਲਬਧ ਹਨ। ਇਹ ਕਈ ਪ੍ਰੋਗਰਾਮਿੰਗ ਭਾਸ਼ਾਵਾਂ ਜਿਵੇਂ C#, Python, JavaScript, Java ਅਤੇ ਹੋਰ ਦੀ ਵਰਤੋਂ ਕਰਨਾ ਸੰਭਵ ਹੈ। ਅਸੀਂ `openai` Python ਲਾਇਬ੍ਰੇਰੀ ਦੀ ਚੋਣ ਕੀਤੀ ਹੈ, ਇਸ ਲਈ ਅਸੀਂ ਇਸਨੂੰ `pip` ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਇੰਸਟਾਲ ਕਰਾਂਗੇ।

```bash
pip install openai
```

### ਇੱਕ ਸਰੋਤ ਬਣਾਓ

ਤੁਹਾਨੂੰ ਹੇਠਾਂ ਦਿੱਤੇ ਕਦਮ ਕਰਨੇ ਪੈਣਗੇ:

- Azure 'ਤੇ ਖਾਤਾ ਬਣਾਓ [https://azure.microsoft.com/free/](https://azure.microsoft.com/free/?WT.mc_id=academic-105485-koreyst)।
- Azure OpenAI ਤੱਕ ਪਹੁੰਚ ਪ੍ਰਾਪਤ ਕਰੋ। [https://learn.microsoft.com/azure/ai-services/openai/overview#how-do-i-get-access-to-azure-openai](https://learn.microsoft.com/azure/ai-services/openai/overview#how-do-i-get-access-to-azure-openai?WT.mc_id=academic-105485-koreyst) 'ਤੇ ਜਾਓ ਅਤੇ ਪਹੁੰਚ ਲਈ ਅਰਜ਼ੀ ਦਿਓ।

  > [!NOTE]
  > ਲਿਖਣ ਦੇ ਸਮੇਂ, ਤੁਹਾਨੂੰ Azure OpenAI ਲਈ ਪਹੁੰਚ ਦੀ ਅਰਜ਼ੀ ਦੇਣੀ ਪੈਂਦੀ ਹੈ।

- Python ਇੰਸਟਾਲ ਕਰੋ <https://www.python.org/>
- Azure OpenAI Service ਸਰੋਤ ਬਣਾਇਆ ਹੋਵੇ। [ਸਰੋਤ ਬਣਾਉਣ](https://learn.microsoft.com/azure/ai-services/openai/how-to/create-resource?pivots=web-portal?WT.mc_id=academic-105485-koreyst) ਲਈ ਇਹ ਗਾਈਡ ਵੇਖੋ।

### API ਕੁੰਜੀ ਅਤੇ ਐਂਡਪੌਇੰਟ ਲੱਭੋ

ਇਸ ਪੜਾਅ 'ਤੇ, ਤੁਹਾਨੂੰ ਆਪਣੀ `openai` ਲਾਇਬ੍ਰੇਰੀ ਨੂੰ ਦੱਸਣਾ ਪਵੇਗਾ ਕਿ ਕਿਹੜੀ API ਕੁੰਜੀ ਵਰਤਣੀ ਹੈ। ਆਪਣੀ API ਕੁੰਜੀ ਲੱਭਣ ਲਈ, Azure OpenAI ਸਰੋਤ ਦੇ "Keys and Endpoint" ਸੈਕਸ਼ਨ 'ਤੇ ਜਾਓ ਅਤੇ "Key 1" ਮੁੱਲ ਕਾਪੀ ਕਰੋ।

![Keys and Endpoint resource blade in Azure Portal](https://learn.microsoft.com/azure/ai-services/openai/media/quickstarts/endpoint.png?WT.mc_id=academic-105485-koreyst)

ਹੁਣ ਜਦੋਂ ਤੁਹਾਡੇ ਕੋਲ ਇਹ ਜਾਣਕਾਰੀ ਕਾਪੀ ਹੈ, ਆਓ ਲਾਇਬ੍ਰੇਰੀਆਂ ਨੂੰ ਇਸਨੂੰ ਵਰਤਣ ਲਈ ਨਿਰਦੇਸ਼ ਦਿੰਦੇ ਹਾਂ।

> [!NOTE]
> ਆਪਣੀ API ਕੁੰਜੀ ਨੂੰ ਆਪਣੇ ਕੋਡ ਤੋਂ ਵੱਖ ਰੱਖਣਾ ਮੁੱਲਵਾਨ ਹੈ। ਤੁਸੀਂ ਇਸਨੂੰ ਵਾਤਾਵਰਣ ਚਰਾਂ (environment variables) ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਕਰ ਸਕਦੇ ਹੋ।
>
> - ਵਾਤਾਵਰਣ ਚਰ `OPENAI_API_KEY` ਨੂੰ ਆਪਣੀ API ਕੁੰਜੀ 'ਤੇ ਸੈਟ ਕਰੋ।
>   `export OPENAI_API_KEY='sk-...'`

### Azure ਕਨਫਿਗਰੇਸ਼ਨ ਸੈਟਅੱਪ

ਜੇ ਤੁਸੀਂ Azure OpenAI ਦੀ ਵਰਤੋਂ ਕਰ ਰਹੇ ਹੋ, ਤਾਂ ਇੱਥੇ ਕਨਫਿਗਰੇਸ਼ਨ ਸੈਟਅੱਪ ਕਰਨ ਦਾ ਤਰੀਕਾ ਹੈ:

```python
openai.api_type = 'azure'
openai.api_key = os.environ["OPENAI_API_KEY"]
openai.api_version = '2023-05-15'
openai.api_base = os.getenv("API_BASE")
```

ਉਪਰ ਅਸੀਂ ਹੇਠਾਂ ਦਿੱਤੇ ਸੈਟ ਕਰ ਰਹੇ ਹਾਂ:

- `api_type` ਨੂੰ `azure`। ਇਹ ਲਾਇਬ੍ਰੇਰੀ ਨੂੰ ਦੱਸਦਾ ਹੈ ਕਿ Azure OpenAI ਦੀ ਵਰਤੋਂ ਕਰਨੀ ਹੈ ਨਾ ਕਿ OpenAI ਦੀ।
- `api_key`, ਇਹ ਤੁਹਾਡੀ API ਕੁੰਜੀ ਹੈ ਜੋ Azure Portal ਵਿੱਚ ਮਿਲਦੀ ਹੈ।
- `api_version`, ਇਹ API ਦਾ ਵਰਜਨ ਹੈ ਜੋ ਤੁਸੀਂ ਵਰਤਣਾ ਚਾਹੁੰਦੇ ਹੋ। ਲਿਖਣ ਦੇ ਸਮੇਂ, ਨਵਾਂ ਵਰਜਨ `2023-05-15` ਹੈ।
- `api_base`, ਇਹ API ਦਾ ਐਂਡਪੌਇੰਟ ਹੈ। ਤੁਸੀਂ ਇਸਨੂੰ Azure Portal ਵਿੱਚ ਆਪਣੀ API ਕੁੰਜੀ ਦੇ ਨਾਲ ਲੱਭ ਸਕਦੇ ਹੋ।

> [!NOTE] > `os.getenv` ਇੱਕ ਫੰਕਸ਼ਨ ਹੈ ਜੋ ਵਾਤਾਵਰਣ ਚਰਾਂ ਨੂੰ ਪੜ੍ਹਦਾ ਹੈ। ਤੁਸੀਂ ਇਸਦੀ ਵਰਤੋਂ `OPENAI_API_KEY` ਅਤੇ `API_BASE` ਵਰਗੇ ਵਾਤਾਵਰਣ ਚਰਾਂ ਨੂੰ ਪੜ੍ਹਨ ਲਈ ਕਰ ਸਕਦੇ ਹੋ। ਇਹ ਵਾਤਾਵਰਣ ਚਰਾਂ ਨੂੰ ਆਪਣੇ ਟਰਮੀਨਲ ਵਿੱਚ ਸੈਟ ਕਰੋ ਜਾਂ `dotenv` ਵਰਗੇ ਲਾਇਬ੍ਰੇਰੀ ਦੀ ਵਰਤੋਂ ਕਰਕੇ।

## ਟੈਕਸਟ ਜਨਰੇਟ ਕਰੋ

ਟੈਕਸਟ ਜਨਰੇਟ ਕਰਨ ਦਾ ਤਰੀਕਾ `Completion` ਕਲਾਸ ਦੀ ਵਰਤੋਂ ਕਰਨਾ ਹੈ। ਇੱਥੇ ਇੱਕ ਉਦਾਹਰਣ ਹੈ:

```python
prompt = "Complete the following: Once upon a time there was a"

completion = openai.Completion.create(model="davinci-002", prompt=prompt)
print(completion.choices[0].text)
```

ਉਪਰਲੇ ਕੋਡ ਵਿੱਚ, ਅਸੀਂ ਇੱਕ Completion ਆਬਜੈਕਟ ਬਣਾਉਂਦੇ ਹਾਂ ਅਤੇ ਮਾਡਲ ਅਤੇ ਪ੍ਰੌਮਪਟ ਪਾਸ ਕਰਦੇ ਹਾਂ। ਫਿਰ ਅਸੀਂ ਜਨਰੇਟ ਕੀਤਾ ਟੈਕਸਟ ਪ੍ਰਿੰਟ ਕਰਦੇ ਹਾਂ।

### ਚੈਟ ਕੰਪਲੀਸ਼ਨਸ

ਹੁਣ ਤੱਕ, ਤੁਸੀਂ ਦੇਖਿਆ ਹੈ ਕਿ ਅਸੀਂ `Completion` ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਟੈਕਸਟ ਜਨਰੇਟ ਕਰ ਰਹੇ ਹਾਂ। ਪਰ ਇੱਕ ਹੋਰ ਕਲਾਸ ਹੈ `ChatCompletion` ਜੋ ਚੈਟਬੋਟਸ ਲਈ ਵਧੇਰੇ ਉਚਿਤ ਹੈ। ਇੱਥੇ ਇਸਦੀ ਵਰਤੋਂ ਦਾ ਉਦਾਹਰਣ ਹੈ:

```python
import openai

openai.api_key = "sk-..."

completion = openai.ChatCompletion.create(model="gpt-3.5-turbo", messages=[{"role": "user", "content": "Hello world"}])
print(completion.choices[0].message.content)
```

ਇਸ ਫੰਕਸ਼ਨਲਿਟੀ ਬਾਰੇ ਹੋਰ ਜਾਣਕਾਰੀ ਅਗਲੇ ਅਧਿਆਇ ਵਿੱਚ।

## ਅਭਿਆਸ - ਆਪਣਾ ਪਹਿਲਾ ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ

ਹੁਣ ਜਦੋਂ ਅਸੀਂ openai ਨੂੰ ਸੈਟਅੱਪ ਅਤੇ ਕਨਫਿਗਰ ਕਰਨ ਦਾ ਤਰੀਕਾ ਸਿੱਖ ਲਿਆ ਹੈ, ਤਾਂ ਆਪਣਾ ਪਹਿਲਾ ਟੈਕਸਟ ਜਨਰੇਸ਼ਨ ਐਪ ਬਣਾਉਣ ਦਾ ਸਮਾਂ ਹੈ। ਐਪ ਬਣਾਉਣ ਲਈ, ਹੇਠਾਂ ਦਿੱਤੇ ਕਦਮਾਂ ਦੀ ਪਾਲਣਾ ਕਰੋ:

1. ਇੱਕ ਵਰਚੁਅਲ ਵਾਤਾਵਰਣ ਬਣਾਓ ਅਤੇ openai ਇੰਸਟਾਲ ਕਰੋ:

   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install openai
   ```

   > [!NOTE]
   > ਜੇ ਤੁਸੀਂ Windows ਦੀ ਵਰਤੋਂ ਕਰ ਰਹੇ ਹੋ ਤਾਂ `venv\Scripts\activate` ਦੀ ਬਜਾਏ `source venv/bin/activate` ਟਾਈਪ ਕਰੋ।

   > [!NOTE]
   > ਆਪਣੀ Azure OpenAI ਕੁੰਜੀ ਲੱਭਣ ਲਈ [https://portal.azure.com/](https://portal.azure.com/?WT.mc_id=academic-105485-koreyst) 'ਤੇ ਜਾਓ ਅਤੇ `Open AI` ਦੀ ਖੋਜ ਕਰੋ ਅਤੇ `Open AI resource` ਚੁਣੋ ਅਤੇ ਫਿਰ `Keys and Endpoint` ਚੁਣੋ ਅਤੇ `Key 1` ਮੁੱਲ ਕਾਪੀ ਕਰੋ।

1. ਇੱਕ _app.py_ ਫਾਈਲ ਬਣਾਓ ਅਤੇ ਇਸ ਵਿੱਚ ਹੇਠਾਂ ਦਿੱਤਾ ਕੋਡ ਦਿਓ:

   ```python
   import openai

   openai.api_key = "<replace this value with your open ai key or Azure OpenAI key>"

   openai.api_type = 'azure'
   openai.api_version = '2023-05-15'
   openai.api_base = "<endpoint found in Azure Portal where your API key is>"
   deployment_name = "<deployment name>"

   # add your completion code
   prompt = "Complete the following: Once upon a time there was a"
   messages = [{"role": "user", "content": prompt}]

   # make completion
   completion = openai.chat.completions.create(model=deployment_name, messages=messages)

   # print response
   print(completion.choices[0].message.content)
   ```

   > [!NOTE]
   > ਜੇ ਤੁਸੀਂ Azure OpenAI ਦੀ ਵਰਤੋਂ ਕਰ ਰਹੇ ਹੋ, ਤਾਂ ਤੁਹਾਨੂੰ `api_type` ਨੂੰ `azure` 'ਤੇ ਸੈਟ ਕਰਨਾ ਪਵੇਗਾ ਅਤੇ `api_key` ਨੂੰ ਆਪਣੀ Azure OpenAI ਕੁੰਜੀ 'ਤੇ ਸੈਟ ਕਰਨਾ ਪਵੇਗਾ।

   ਤੁਹਾਨੂੰ ਹੇਠਾਂ ਦਿੱਤੇ ਵਰਗਾ ਨਤੀਜਾ ਦੇਖਣ ਨੂੰ ਮਿਲੇਗਾ:

   ```output
    very unhappy _____.

   Once upon a time there was a very unhappy mermaid.
   ```

## ਵੱਖ-ਵੱਖ ਤਰ੍ਹਾਂ ਦੇ ਪ੍ਰੌਮਪਟਸ, ਵੱਖ-ਵੱਖ ਕੰਮਾਂ ਲਈ

ਹੁਣ ਤੁਸੀਂ ਦੇਖਿਆ ਹੈ ਕਿ ਪ੍ਰੌਮਪਟ ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਟੈਕਸਟ ਕਿਵੇਂ ਜਨਰੇਟ ਕੀਤਾ ਜਾ ਸਕਦਾ ਹੈ। ਤੁਹਾਡੇ ਕੋਲ ਇੱਕ ਪ੍ਰੋਗਰਾਮ ਹੈ ਜੋ ਤੁਸੀਂ ਸੋਧ ਅਤੇ ਬਦਲ ਸਕਦੇ ਹੋ ਤਾਂ ਕਿ ਵੱਖ-ਵੱਖ ਤਰ੍ਹਾਂ ਦਾ ਟੈਕਸਟ ਜਨਰੇਟ ਕੀਤਾ ਜਾ ਸਕੇ।

ਪ੍ਰੌਮਪਟਸ ਕਈ ਤਰ੍ਹਾਂ ਦੇ ਕੰਮਾਂ ਲਈ ਵਰਤੇ ਜਾ ਸਕਦੇ ਹਨ। ਉਦਾਹਰਣ ਲਈ:

- **ਇੱਕ ਕਿਸਮ ਦਾ ਟੈਕਸਟ ਜਨਰੇਟ ਕਰੋ**। ਉਦਾਹਰਣ ਲਈ, ਤੁਸੀਂ ਇੱਕ ਕਵਿਤਾ, ਕਵਿਜ ਲਈ ਸਵਾਲ ਆਦਿ ਜਨਰੇਟ ਕਰ ਸਕਦੇ ਹੋ।
- **ਜਾਣਕਾਰੀ ਲੱਭੋ**। ਤੁਸੀਂ ਪ੍ਰੌਮਪਟਸ ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਜਾਣਕਾਰੀ ਲੱਭ ਸਕਦੇ ਹੋ ਜਿਵੇਂ 'What does CORS mean in web development?'।
- **ਕੋਡ ਜਨਰੇਟ ਕਰੋ**। ਤੁਸੀਂ ਪ੍ਰੌਮਪਟਸ ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਕੋਡ ਜਨਰੇਟ ਕਰ ਸਕਦੇ ਹੋ, ਉਦਾਹਰਣ ਲਈ, ਇੱਕ ਰੈਗੂਲਰ ਐਕਸਪ੍ਰੈਸ਼ਨ ਵਿਕਸਿਤ ਕਰਨਾ ਜੋ ਈਮੇਲਾਂ ਨੂੰ ਵੈਰੀਫਾਈ ਕਰਦਾ ਹੈ ਜਾਂ ਇੱਕ ਪੂਰਾ ਪ੍ਰੋਗਰਾਮ ਜਨਰੇਟ ਕਰਨਾ, ਜਿਵੇਂ ਕਿ ਇੱਕ ਵੈੱਬ ਐਪ।

## ਇੱਕ ਹੋਰ ਵਿਆਹਾਰਕ ਉਦਾਹਰਣ: ਰੈਸੀਪੀ ਜਨਰੇਟਰ

ਕਲਪਨਾ ਕਰੋ ਕਿ ਤੁਹਾਡੇ ਕੋਲ ਘਰ ਵਿੱਚ ਸਮੱਗਰੀ ਹੈ ਅਤੇ ਤੁਸੀਂ ਕੁਝ ਪਕਾਉਣਾ ਚਾਹੁੰਦੇ ਹੋ। ਇਸ ਲਈ, ਤੁਹਾਨੂੰ ਇੱਕ ਰੈਸੀਪੀ ਦੀ ਲੋੜ ਹੈ। ਰੈਸੀਪੀ ਲੱਭਣ ਦਾ ਇੱਕ ਤਰੀਕਾ ਸਰਚ ਇੰਜਨ ਦੀ ਵਰਤੋਂ ਕਰਨਾ ਹੈ ਜਾਂ ਤੁਸੀਂ ਇਸ ਲਈ ਇੱਕ LLM ਦੀ ਵਰਤੋਂ ਕਰ ਸਕਦੇ ਹੋ।

ਤੁਸੀਂ ਇੱਕ ਪ੍ਰੌਮਪਟ ਇਸ ਤਰ੍ਹਾਂ ਲਿਖ ਸਕਦੇ ਹੋ:

>
ਕੋਡ ਵਿੱਚ ਉਸ ਹਿੱਸੇ ਨੂੰ ਲੱਭੋ ਜੋ ਪਹਿਲੇ ਪ੍ਰੰਪਟ ਤੋਂ ਨਤੀਜਾ ਪ੍ਰਿੰਟ ਕਰਦਾ ਹੈ ਅਤੇ ਹੇਠਾਂ ਦਿੱਤਾ ਕੋਡ ਸ਼ਾਮਲ ਕਰੋ:

  ```python
  old_prompt_result = completion.choices[0].message.content
  prompt = "Produce a shopping list for the generated recipes and please don't include ingredients that I already have."

  new_prompt = f"{old_prompt_result} {prompt}"
  messages = [{"role": "user", "content": new_prompt}]
  completion = openai.Completion.create(engine=deployment_name, messages=messages, max_tokens=1200)

  # print response
  print("Shopping list:")
  print(completion.choices[0].message.content)
  ```

ਹੇਠਾਂ ਦਿੱਤੇ ਬਿੰਦੂਆਂ ਨੂੰ ਯਾਦ ਰੱਖੋ:

1. ਅਸੀਂ ਇੱਕ ਨਵਾਂ ਪ੍ਰੰਪਟ ਬਣਾਉਣ ਲਈ ਪਹਿਲੇ ਪ੍ਰੰਪਟ ਦੇ ਨਤੀਜੇ ਨੂੰ ਨਵੇਂ ਪ੍ਰੰਪਟ ਵਿੱਚ ਸ਼ਾਮਲ ਕਰ ਰਹੇ ਹਾਂ:

     ```python
     new_prompt = f"{old_prompt_result} {prompt}"
     ```

1. ਅਸੀਂ ਇੱਕ ਨਵੀਂ ਬੇਨਤੀ ਕਰਦੇ ਹਾਂ, ਪਰ ਪਹਿਲੇ ਪ੍ਰੰਪਟ ਵਿੱਚ ਮੰਗੇ ਗਏ ਟੋਕਨ ਦੀ ਗਿਣਤੀ ਨੂੰ ਵੀ ਧਿਆਨ ਵਿੱਚ ਰੱਖਦੇ ਹਾਂ, ਇਸ ਲਈ ਇਸ ਵਾਰ ਅਸੀਂ `max_tokens` ਨੂੰ 1200 ਕਹਿੰਦੇ ਹਾਂ।

     ```python
     completion = openai.Completion.create(engine=deployment_name, prompt=new_prompt, max_tokens=1200)
     ```

ਇਸ ਕੋਡ ਨੂੰ ਚਲਾਉਣ ਨਾਲ, ਅਸੀਂ ਹੁਣ ਹੇਠਾਂ ਦਿੱਤੇ ਨਤੀਜੇ 'ਤੇ ਪਹੁੰਚਦੇ ਹਾਂ:

     ```output
     No of recipes (for example, 5): 2
     List of ingredients (for example, chicken, potatoes, and carrots): apple,flour
     Filter (for example, vegetarian, vegan, or gluten-free): sugar


     -Apple and flour pancakes: 1 cup flour, 1/2 tsp baking powder, 1/2 tsp baking soda, 1/4 tsp salt, 1 tbsp sugar, 1 egg, 1 cup buttermilk or sour milk, 1/4 cup melted butter, 1 Granny Smith apple, peeled and grated
     -Apple fritters: 1-1/2 cups flour, 1 tsp baking powder, 1/4 tsp salt, 1/4 tsp baking soda, 1/4 tsp nutmeg, 1/4 tsp cinnamon, 1/4 tsp allspice, 1/4 cup sugar, 1/4 cup vegetable shortening, 1/4 cup milk, 1 egg, 2 cups shredded, peeled apples
     Shopping list:
     -Flour, baking powder, baking soda, salt, sugar, egg, buttermilk, butter, apple, nutmeg, cinnamon, allspice
     ```

## ਆਪਣੀ ਸੈਟਅੱਪ ਨੂੰ ਬਿਹਤਰ ਬਣਾਓ

ਜੋ ਕੁਝ ਅਸੀਂ ਹੁਣ ਤੱਕ ਕੀਤਾ ਹੈ ਉਹ ਕੰਮ ਕਰਦਾ ਹੈ, ਪਰ ਕੁਝ ਸੁਧਾਰ ਹਨ ਜੋ ਅਸੀਂ ਚੀਜ਼ਾਂ ਨੂੰ ਹੋਰ ਬਿਹਤਰ ਬਣਾਉਣ ਲਈ ਕਰਨੇ ਚਾਹੀਦੇ ਹਨ। ਕੁਝ ਚੀਜ਼ਾਂ ਜੋ ਅਸੀਂ ਕਰ ਸਕਦੇ ਹਾਂ:

- **ਰਹੱਸਾਂ ਨੂੰ ਕੋਡ ਤੋਂ ਵੱਖ ਕਰੋ**, ਜਿਵੇਂ ਕਿ API ਕੁੰਜੀ। ਰਹੱਸਾਂ ਕੋਡ ਵਿੱਚ ਨਹੀਂ ਹੋਣੇ ਚਾਹੀਦੇ ਅਤੇ ਸੁਰੱਖਿਅਤ ਸਥਾਨ ਵਿੱਚ ਸਟੋਰ ਕੀਤੇ ਜਾਣੇ ਚਾਹੀਦੇ ਹਨ। ਰਹੱਸਾਂ ਨੂੰ ਕੋਡ ਤੋਂ ਵੱਖ ਕਰਨ ਲਈ, ਅਸੀਂ ਵਾਤਾਵਰਣ ਵੈਰੀਏਬਲ ਅਤੇ `python-dotenv` ਵਰਗੀਆਂ ਲਾਇਬ੍ਰੇਰੀਆਂ ਦੀ ਵਰਤੋਂ ਕਰ ਸਕਦੇ ਹਾਂ ਤਾਂ ਜੋ ਉਹਨਾਂ ਨੂੰ ਫਾਈਲ ਤੋਂ ਲੋਡ ਕੀਤਾ ਜਾ ਸਕੇ। ਇਹ ਕੋਡ ਵਿੱਚ ਇਸ ਤਰ੍ਹਾਂ ਦੇਖਾਈ ਦੇਵੇਗਾ:

1. ਇੱਕ `.env` ਫਾਈਲ ਬਣਾਓ ਜਿਸ ਵਿੱਚ ਹੇਠਾਂ ਦਿੱਤਾ ਸਮੱਗਰੀ ਹੋਵੇ:

     ```bash
     OPENAI_API_KEY=sk-...
     ```

> ਨੋਟ ਕਰੋ, Azure ਲਈ, ਤੁਹਾਨੂੰ ਹੇਠਾਂ ਦਿੱਤੇ ਵਾਤਾਵਰਣ ਵੈਰੀਏਬਲ ਸੈਟ ਕਰਨ ਦੀ ਲੋੜ ਹੈ:

     ```bash
     OPENAI_API_TYPE=azure
     OPENAI_API_VERSION=2023-05-15
     OPENAI_API_BASE=<replace>
     ```

ਕੋਡ ਵਿੱਚ, ਤੁਸੀਂ ਵਾਤਾਵਰਣ ਵੈਰੀਏਬਲ ਨੂੰ ਇਸ ਤਰ੍ਹਾਂ ਲੋਡ ਕਰੋਗੇ:

     ```python
     from dotenv import load_dotenv

     load_dotenv()

     openai.api_key = os.environ["OPENAI_API_KEY"]
     ```

- **ਟੋਕਨ ਦੀ ਲੰਬਾਈ ਬਾਰੇ ਇੱਕ ਗੱਲ**। ਅਸੀਂ ਇਹ ਵਿਚਾਰ ਕਰਨਾ ਚਾਹੀਦਾ ਹੈ ਕਿ ਸਾਨੂੰ ਉਹ ਟੈਕਸਟ ਜਨਰੇਟ ਕਰਨ ਲਈ ਕਿੰਨੇ ਟੋਕਨ ਦੀ ਲੋੜ ਹੈ ਜੋ ਅਸੀਂ ਚਾਹੁੰਦੇ ਹਾਂ। ਟੋਕਨ ਪੈਸੇ ਖਰਚਦੇ ਹਨ, ਇਸ ਲਈ ਜਿੱਥੇ ਸੰਭਵ ਹੋਵੇ, ਅਸੀਂ ਵਰਤੇ ਗਏ ਟੋਕਨ ਦੀ ਗਿਣਤੀ ਨਾਲ ਆਰਥਿਕ ਹੋਣ ਦੀ ਕੋਸ਼ਿਸ਼ ਕਰਨੀ ਚਾਹੀਦੀ ਹੈ। ਉਦਾਹਰਣ ਲਈ, ਕੀ ਅਸੀਂ ਪ੍ਰੰਪਟ ਨੂੰ ਇਸ ਤਰ੍ਹਾਂ ਫਰੇਜ਼ ਕਰ ਸਕਦੇ ਹਾਂ ਕਿ ਅਸੀਂ ਘੱਟ ਟੋਕਨ ਦੀ ਵਰਤੋਂ ਕਰ ਸਕੀਏ?

ਟੋਕਨ ਦੀ ਵਰਤੋਂ ਨੂੰ ਬਦਲਣ ਲਈ, ਤੁਸੀਂ `max_tokens` ਪੈਰਾਮੀਟਰ ਦੀ ਵਰਤੋਂ ਕਰ ਸਕਦੇ ਹੋ। ਉਦਾਹਰਣ ਲਈ, ਜੇ ਤੁਸੀਂ 100 ਟੋਕਨ ਦੀ ਵਰਤੋਂ ਕਰਨਾ ਚਾਹੁੰਦੇ ਹੋ, ਤਾਂ ਤੁਸੀਂ ਇਹ ਕਰੋਗੇ:

  ```python
  completion = client.chat.completions.create(model=deployment, messages=messages, max_tokens=100)
  ```

- **ਤਾਪਮਾਨ ਨਾਲ ਪ੍ਰਯੋਗ ਕਰਨਾ**। ਤਾਪਮਾਨ ਇੱਕ ਅਹਿਮ ਸੰਦਰਭ ਹੈ ਜਿਸ ਬਾਰੇ ਅਸੀਂ ਹੁਣ ਤੱਕ ਗੱਲ ਨਹੀਂ ਕੀਤੀ ਹੈ ਪਰ ਇਹ ਸਾਡੇ ਪ੍ਰੋਗਰਾਮ ਦੇ ਕੰਮ ਕਰਨ ਦੇ ਤਰੀਕੇ ਲਈ ਮਹੱਤਵਪੂਰਨ ਹੈ। ਤਾਪਮਾਨ ਦਾ ਮੁੱਲ ਜਿੰਨਾ ਜ਼ਿਆਦਾ ਹੋਵੇਗਾ, ਨਤੀਜਾ ਉਤਨਾ ਹੀ ਬੇਤਰਤੀਬ ਹੋਵੇਗਾ। ਇਸਦੇ ਉਲਟ, ਤਾਪਮਾਨ ਦਾ ਮੁੱਲ ਜਿੰਨਾ ਘੱਟ ਹੋਵੇਗਾ, ਨਤੀਜਾ ਉਤਨਾ ਹੀ ਅਨੁਮਾਨਯੋਗ ਹੋਵੇਗਾ। ਇਹ ਵਿਚਾਰ ਕਰੋ ਕਿ ਕੀ ਤੁਸੀਂ ਆਪਣੇ ਨਤੀਜੇ ਵਿੱਚ ਵੱਖ-ਵੱਖਤਾ ਚਾਹੁੰਦੇ ਹੋ ਜਾਂ ਨਹੀਂ।

ਤਾਪਮਾਨ ਨੂੰ ਬਦਲਣ ਲਈ, ਤੁਸੀਂ `temperature` ਪੈਰਾਮੀਟਰ ਦੀ ਵਰਤੋਂ ਕਰ ਸਕਦੇ ਹੋ। ਉਦਾਹਰਣ ਲਈ, ਜੇ ਤੁਸੀਂ 0.5 ਦਾ ਤਾਪਮਾਨ ਵਰਤਣਾ ਚਾਹੁੰਦੇ ਹੋ, ਤਾਂ ਤੁਸੀਂ ਇਹ ਕਰੋਗੇ:

  ```python
  completion = client.chat.completions.create(model=deployment, messages=messages, temperature=0.5)
  ```

> ਨੋਟ ਕਰੋ, 1.0 ਦੇ ਨੇੜੇ, ਨਤੀਜਾ ਜ਼ਿਆਦਾ ਵੱਖ-ਵੱਖ ਹੋਵੇਗਾ।

## ਅਸਾਈਨਮੈਂਟ

ਇਸ ਅਸਾਈਨਮੈਂਟ ਲਈ, ਤੁਸੀਂ ਕੀ ਬਣਾਉਣਾ ਹੈ, ਚੁਣ ਸਕਦੇ ਹੋ।

ਇੱਥੇ ਕੁਝ ਸੁਝਾਅ ਹਨ:

- ਰੈਸਿਪੀ ਜਨਰੇਟਰ ਐਪ ਨੂੰ ਹੋਰ ਬਿਹਤਰ ਬਣਾਉਣ ਲਈ ਸੁਧਾਰ ਕਰੋ। ਤਾਪਮਾਨ ਦੇ ਮੁੱਲਾਂ ਨਾਲ ਖੇਡੋ ਅਤੇ ਪ੍ਰੰਪਟਾਂ ਨਾਲ ਅਨੁਸੰਧਾਨ ਕਰੋ ਕਿ ਤੁਸੀਂ ਕੀ ਬਣਾਉਣ ਦੇ ਯੋਗ ਹੋ।
- ਇੱਕ "ਅਧਿਐਨ ਸਾਥੀ" ਬਣਾਓ। ਇਹ ਐਪ ਕਿਸੇ ਵਿਸ਼ੇ ਬਾਰੇ ਸਵਾਲਾਂ ਦੇ ਜਵਾਬ ਦੇਣ ਦੇ ਯੋਗ ਹੋਣਾ ਚਾਹੀਦਾ ਹੈ, ਉਦਾਹਰਣ ਲਈ ਪਾਇਥਨ, ਤੁਸੀਂ "ਪਾਇਥਨ ਵਿੱਚ ਇੱਕ ਵਿਸ਼ੇ ਕੀ ਹੈ?" ਵਰਗੇ ਪ੍ਰੰਪਟਾਂ ਰੱਖ ਸਕਦੇ ਹੋ, ਜਾਂ ਤੁਸੀਂ ਇੱਕ ਪ੍ਰੰਪਟ ਰੱਖ ਸਕਦੇ ਹੋ ਜੋ ਕਹਿੰਦਾ ਹੈ, ਮੈਨੂੰ ਇੱਕ ਵਿਸ਼ੇ ਲਈ ਕੋਡ ਦਿਖਾਓ ਆਦਿ।
- ਇਤਿਹਾਸ ਬੋਟ, ਇਤਿਹਾਸ ਨੂੰ ਜਿਊਂਦਾ ਬਣਾਓ, ਬੋਟ ਨੂੰ ਇੱਕ ਵਿਸ਼ੇਸ਼ ਇਤਿਹਾਸਕ ਪਾਤਰ ਬਣਨ ਲਈ ਕਹੋ ਅਤੇ ਉਸਦੇ ਜੀਵਨ ਅਤੇ ਸਮੇਂ ਬਾਰੇ ਸਵਾਲ ਪੁੱਛੋ।

## ਹੱਲ

### ਅਧਿਐਨ ਸਾਥੀ

ਹੇਠਾਂ ਇੱਕ ਸ਼ੁਰੂਆਤੀ ਪ੍ਰੰਪਟ ਹੈ, ਵੇਖੋ ਕਿ ਤੁਸੀਂ ਇਸਨੂੰ ਕਿਵੇਂ ਵਰਤ ਸਕਦੇ ਹੋ ਅਤੇ ਇਸਨੂੰ ਆਪਣੇ ਪਸੰਦ ਅਨੁਸਾਰ ਕਿਵੇਂ ਬਦਲ ਸਕਦੇ ਹੋ।

```text
- "You're an expert on the Python language

    Suggest a beginner lesson for Python in the following format:

    Format:
    - concepts:
    - brief explanation of the lesson:
    - exercise in code with solutions"
```

### ਇਤਿਹਾਸ ਬੋਟ

ਇੱਥੇ ਕੁਝ ਪ੍ਰੰਪਟ ਹਨ ਜੋ ਤੁਸੀਂ ਵਰਤ ਸਕਦੇ ਹੋ:

```text
- "You are Abe Lincoln, tell me about yourself in 3 sentences, and respond using grammar and words like Abe would have used"
- "You are Abe Lincoln, respond using grammar and words like Abe would have used:

   Tell me about your greatest accomplishments, in 300 words"
```

## ਗਿਆਨ ਦੀ ਜਾਂਚ

ਤਾਪਮਾਨ ਦਾ ਅਰਥ ਕੀ ਹੈ?

1. ਇਹ ਨਤੀਜੇ ਨੂੰ ਕਿੰਨਾ ਬੇਤਰਤੀਬ ਬਣਾਉਂਦਾ ਹੈ, ਇਸਨੂੰ ਨਿਯੰਤਰਿਤ ਕਰਦਾ ਹੈ।
1. ਇਹ ਜਵਾਬ ਕਿੰਨਾ ਵੱਡਾ ਹੈ, ਇਸਨੂੰ ਨਿਯੰਤਰਿਤ ਕਰਦਾ ਹੈ।
1. ਇਹ ਵਰਤੇ ਗਏ ਟੋਕਨ ਦੀ ਗਿਣਤੀ ਨੂੰ ਨਿਯੰਤਰਿਤ ਕਰਦਾ ਹੈ।

## 🚀 ਚੁਣੌਤੀ

ਅਸਾਈਨਮੈਂਟ 'ਤੇ ਕੰਮ ਕਰਦੇ ਸਮੇਂ, ਤਾਪਮਾਨ ਵਿੱਚ ਵੱਖ-ਵੱਖਤਾ ਲਿਆਓ, ਇਸਨੂੰ 0, 0.5, ਅਤੇ 1 'ਤੇ ਸੈਟ ਕਰਨ ਦੀ ਕੋਸ਼ਿਸ਼ ਕਰੋ। ਯਾਦ ਰੱਖੋ ਕਿ 0 ਸਭ ਤੋਂ ਘੱਟ ਵੱਖ-ਵੱਖ ਹੈ ਅਤੇ 1 ਸਭ ਤੋਂ ਵੱਧ ਹੈ। ਤੁਹਾਡੇ ਐਪ ਲਈ ਕਿਹੜਾ ਮੁੱਲ ਸਭ ਤੋਂ ਵਧੀਆ ਕੰਮ ਕਰਦਾ ਹੈ?

## ਸ਼ਾਨਦਾਰ ਕੰਮ! ਆਪਣਾ ਸਿੱਖਣਾ ਜਾਰੀ ਰੱਖੋ

ਇਹ ਪਾਠ ਪੂਰਾ ਕਰਨ ਤੋਂ ਬਾਅਦ, ਆਪਣਾ ਜਨਰੇਟਿਵ AI ਗਿਆਨ ਵਧਾਉਣ ਲਈ [Generative AI Learning collection](https://aka.ms/genai-collection?WT.mc_id=academic-105485-koreyst) 'ਤੇ ਜਾਓ!

ਪਾਠ 7 'ਤੇ ਜਾਓ ਜਿੱਥੇ ਅਸੀਂ ਦੇਖਾਂਗੇ ਕਿ [ਚੈਟ ਐਪਲੀਕੇਸ਼ਨ ਕਿਵੇਂ ਬਣਾਉਣੀਆਂ ਹਨ](../07-building-chat-applications/README.md?WT.mc_id=academic-105485-koreyst)!

---

**ਅਸਵੀਕਰਤਾ**:  
ਇਹ ਦਸਤਾਵੇਜ਼ AI ਅਨੁਵਾਦ ਸੇਵਾ [Co-op Translator](https://github.com/Azure/co-op-translator) ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਅਨੁਵਾਦ ਕੀਤਾ ਗਿਆ ਹੈ। ਜਦੋਂ ਕਿ ਅਸੀਂ ਸਹੀ ਹੋਣ ਦੀ ਕੋਸ਼ਿਸ਼ ਕਰਦੇ ਹਾਂ, ਕਿਰਪਾ ਕਰਕੇ ਧਿਆਨ ਦਿਓ ਕਿ ਸਵੈਚਾਲਿਤ ਅਨੁਵਾਦਾਂ ਵਿੱਚ ਗਲਤੀਆਂ ਜਾਂ ਅਸੁਚੀਤਤਾਵਾਂ ਹੋ ਸਕਦੀਆਂ ਹਨ। ਇਸ ਦੀ ਮੂਲ ਭਾਸ਼ਾ ਵਿੱਚ ਮੂਲ ਦਸਤਾਵੇਜ਼ ਨੂੰ ਅਧਿਕਾਰਤ ਸਰੋਤ ਮੰਨਿਆ ਜਾਣਾ ਚਾਹੀਦਾ ਹੈ। ਮਹੱਤਵਪੂਰਨ ਜਾਣਕਾਰੀ ਲਈ, ਪੇਸ਼ੇਵਰ ਮਨੁੱਖੀ ਅਨੁਵਾਦ ਦੀ ਸਿਫਾਰਸ਼ ਕੀਤੀ ਜਾਂਦੀ ਹੈ। ਇਸ ਅਨੁਵਾਦ ਦੀ ਵਰਤੋਂ ਤੋਂ ਪੈਦਾ ਹੋਣ ਵਾਲੇ ਕਿਸੇ ਵੀ ਗਲਤਫਹਿਮੀ ਜਾਂ ਗਲਤ ਵਿਆਖਿਆ ਲਈ ਅਸੀਂ ਜ਼ਿੰਮੇਵਾਰ ਨਹੀਂ ਹਾਂ।