<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "00e33cd3ff945511446ecda4a9f8a828",
  "translation_date": "2025-10-17T13:45:00+00:00",
  "source_file": "06-text-generation-apps/README.md",
  "language_code": "mr"
}
-->
# टेक्स्ट जनरेशन अॅप्लिकेशन्स तयार करणे

[![टेक्स्ट जनरेशन अॅप्लिकेशन्स तयार करणे](../../../translated_images/06-lesson-banner.a5c629f990a636c852353c5533f1a6a218ece579005e91f96339d508d9cf8f47.mr.png)](https://youtu.be/0Y5Luf5sRQA?si=t_xVg0clnAI4oUFZ)

> _(वरील प्रतिमेवर क्लिक करून या धड्याचा व्हिडिओ पहा)_

या अभ्यासक्रमाद्वारे तुम्ही आतापर्यंत पाहिले आहे की प्रॉम्प्ट्ससारख्या मुख्य संकल्पना आहेत आणि "प्रॉम्प्ट इंजिनिअरिंग" नावाचा एक संपूर्ण विषय आहे. ChatGPT, Office 365, Microsoft Power Platform आणि इतर अनेक साधने तुम्हाला प्रॉम्प्ट्स वापरून काहीतरी साध्य करण्यासाठी समर्थन देतात.

तुमच्या अॅपमध्ये अशा अनुभवाची भर घालण्यासाठी, तुम्हाला प्रॉम्प्ट्स, कंप्लीशन्स यासारख्या संकल्पना समजून घेणे आवश्यक आहे आणि काम करण्यासाठी एक लायब्ररी निवडावी लागेल. याच गोष्टी तुम्ही या अध्यायात शिकाल.

## परिचय

या अध्यायात तुम्ही:

- openai लायब्ररी आणि तिच्या मुख्य संकल्पनांबद्दल शिकाल.
- openai वापरून एक टेक्स्ट जनरेशन अॅप तयार कराल.
- प्रॉम्प्ट, टेम्परेचर आणि टोकन्स यासारख्या संकल्पना वापरून टेक्स्ट जनरेशन अॅप कसे तयार करायचे ते समजून घ्याल.

## शिकण्याची उद्दिष्टे

या धड्याच्या शेवटी, तुम्ही:

- टेक्स्ट जनरेशन अॅप म्हणजे काय ते स्पष्ट करू शकाल.
- openai वापरून टेक्स्ट जनरेशन अॅप तयार करू शकाल.
- तुमच्या अॅपमध्ये अधिक किंवा कमी टोकन्स वापरण्यासाठी आणि टेम्परेचर बदलण्यासाठी कॉन्फिगर करू शकाल, ज्यामुळे विविध आउटपुट मिळेल.

## टेक्स्ट जनरेशन अॅप म्हणजे काय?

सामान्यतः जेव्हा तुम्ही अॅप तयार करता तेव्हा त्यामध्ये खालीलप्रमाणे काही प्रकारचे इंटरफेस असते:

- कमांड-आधारित. कन्सोल अॅप्स हे सामान्यतः असे अॅप्स असतात जिथे तुम्ही कमांड टाइप करता आणि ते कार्य पूर्ण करते. उदाहरणार्थ, `git` हे एक कमांड-आधारित अॅप आहे.
- युजर इंटरफेस (UI). काही अॅप्समध्ये ग्राफिकल युजर इंटरफेस (GUIs) असतात जिथे तुम्ही बटणे क्लिक करता, टेक्स्ट इनपुट करता, पर्याय निवडता आणि बरेच काही करता.

### कन्सोल आणि UI अॅप्स मर्यादित आहेत

कमांड-आधारित अॅपशी तुलना करा जिथे तुम्ही कमांड टाइप करता:

- **मर्यादित आहे**. तुम्ही कोणताही कमांड टाइप करू शकत नाही, फक्त अॅपने समर्थन दिलेले कमांड्सच टाइप करू शकता.
- **भाषा-विशिष्ट**. काही अॅप्स अनेक भाषांना समर्थन देतात, परंतु डीफॉल्टनुसार अॅप विशिष्ट भाषेसाठी तयार केले जाते, जरी तुम्ही अधिक भाषा समर्थन जोडू शकता.

### टेक्स्ट जनरेशन अॅप्सचे फायदे

मग टेक्स्ट जनरेशन अॅप वेगळे कसे आहे?

टेक्स्ट जनरेशन अॅपमध्ये तुम्हाला अधिक लवचिकता मिळते, तुम्ही कमांड्सच्या सेट किंवा विशिष्ट इनपुट भाषेपुरते मर्यादित नसता. त्याऐवजी, तुम्ही अॅपशी संवाद साधण्यासाठी नैसर्गिक भाषा वापरू शकता. आणखी एक फायदा म्हणजे तुम्ही आधीच मोठ्या प्रमाणावर माहितीवर प्रशिक्षित डेटासोर्सशी संवाद साधत आहात, तर पारंपरिक अॅप डेटाबेसमध्ये असलेल्या गोष्टींवर मर्यादित असतो.

### टेक्स्ट जनरेशन अॅपसह मी काय तयार करू शकतो?

तुम्ही अनेक गोष्टी तयार करू शकता. उदाहरणार्थ:

- **चॅटबॉट**. तुमच्या कंपनी आणि तिच्या उत्पादनांबद्दल प्रश्नांची उत्तरे देणारा चॅटबॉट एक चांगला पर्याय असू शकतो.
- **मदतनीस**. LLMs टेक्स्टचे सारांश तयार करणे, टेक्स्टमधून अंतर्दृष्टी मिळवणे, रिझ्युमेसारखा टेक्स्ट तयार करणे यासारख्या गोष्टींसाठी उत्कृष्ट आहेत.
- **कोड सहाय्यक**. तुम्ही वापरत असलेल्या भाषा मॉडेलवर अवलंबून, तुम्ही कोड लिहिण्यास मदत करणारा कोड सहाय्यक तयार करू शकता. उदाहरणार्थ, तुम्ही GitHub Copilot तसेच ChatGPT सारख्या उत्पादनांचा वापर करून कोड लिहिण्यास मदत करू शकता.

## मी कसे सुरुवात करू शकतो?

ठीक आहे, तुम्हाला LLM सह एकत्रिकरण करण्याचा मार्ग शोधावा लागेल, ज्यामध्ये सामान्यतः खालील दोन पद्धतींचा समावेश होतो:

- API वापरा. येथे तुम्ही तुमच्या प्रॉम्प्टसह वेब विनंत्या तयार करत आहात आणि तयार केलेला टेक्स्ट परत मिळवत आहात.
- लायब्ररी वापरा. लायब्ररी API कॉल्स कॅप्सुलेट करण्यात मदत करतात आणि त्यांचा वापर सुलभ करतात.

## लायब्ररी/SDKs

LLMsसह काम करण्यासाठी काही सुप्रसिद्ध लायब्ररी आहेत जसे की:

- **openai**, ही लायब्ररी तुमच्या मॉडेलशी कनेक्ट होणे आणि प्रॉम्प्ट्स पाठवणे सोपे करते.

त्यानंतर उच्च स्तरावर कार्य करणाऱ्या लायब्ररी आहेत जसे की:

- **Langchain**. Langchain सुप्रसिद्ध आहे आणि Python ला समर्थन देते.
- **Semantic Kernel**. Semantic Kernel ही Microsoft ची लायब्ररी आहे जी C#, Python आणि Java भाषांना समर्थन देते.

## openai वापरून पहिला अॅप

चला पाहूया की आपण आपला पहिला अॅप कसा तयार करू शकतो, कोणत्या लायब्ररीची आवश्यकता आहे, किती आवश्यक आहे इत्यादी.

### openai इंस्टॉल करा

OpenAI किंवा Azure OpenAI सह संवाद साधण्यासाठी अनेक लायब्ररी उपलब्ध आहेत. C#, Python, JavaScript, Java आणि इतर अनेक प्रोग्रामिंग भाषा वापरणे शक्य आहे. आम्ही `openai` Python लायब्ररी वापरण्यास निवडले आहे, त्यामुळे आम्ही `pip` वापरून ती इंस्टॉल करू.

```bash
pip install openai
```

### संसाधन तयार करा

तुम्हाला खालील चरण पूर्ण करणे आवश्यक आहे:

- Azure वर खाते तयार करा [https://azure.microsoft.com/free/](https://azure.microsoft.com/free/?WT.mc_id=academic-105485-koreyst).
- Azure OpenAI वर प्रवेश मिळवा. [https://learn.microsoft.com/azure/ai-services/openai/overview#how-do-i-get-access-to-azure-openai](https://learn.microsoft.com/azure/ai-services/openai/overview#how-do-i-get-access-to-azure-openai?WT.mc_id=academic-105485-koreyst) येथे जा आणि प्रवेशासाठी विनंती करा.

  > [!NOTE]
  > लेखनाच्या वेळी, तुम्हाला Azure OpenAI साठी प्रवेशासाठी अर्ज करणे आवश्यक आहे.

- Python इंस्टॉल करा <https://www.python.org/>
- Azure OpenAI सेवा संसाधन तयार केले आहे. [संसाधन तयार करण्यासाठी मार्गदर्शक](https://learn.microsoft.com/azure/ai-services/openai/how-to/create-resource?pivots=web-portal?WT.mc_id=academic-105485-koreyst) पहा.

### API की आणि एंडपॉइंट शोधा

या टप्प्यावर, तुम्हाला तुमच्या `openai` लायब्ररीला कोणती API की वापरायची ते सांगावे लागेल. तुमची API की शोधण्यासाठी, Azure OpenAI संसाधनाच्या "Keys and Endpoint" विभागात जा आणि "Key 1" मूल्य कॉपी करा.

![Azure पोर्टलमधील Keys and Endpoint संसाधन ब्लेड](https://learn.microsoft.com/azure/ai-services/openai/media/quickstarts/endpoint.png?WT.mc_id=academic-105485-koreyst)

आता तुमच्याकडे ही माहिती कॉपी केली आहे, चला लायब्ररींना ती वापरण्यास सांगूया.

> [!NOTE]
> तुमची API की तुमच्या कोडपासून वेगळी ठेवणे योग्य आहे. तुम्ही पर्यावरणीय व्हेरिएबल्स वापरून हे करू शकता.
>
> - पर्यावरणीय व्हेरिएबल `OPENAI_API_KEY` तुमच्या API की वर सेट करा.
>   `export OPENAI_API_KEY='sk-...'`

### Azure कॉन्फिगरेशन सेटअप करा

जर तुम्ही Azure OpenAI वापरत असाल, तर कॉन्फिगरेशन कसे सेट करायचे ते येथे आहे:

```python
openai.api_type = 'azure'
openai.api_key = os.environ["OPENAI_API_KEY"]
openai.api_version = '2023-05-15'
openai.api_base = os.getenv("API_BASE")
```

वरीलमध्ये आम्ही खालील सेट करत आहोत:

- `api_type` `azure` वर सेट केले आहे. हे लायब्ररीला OpenAI ऐवजी Azure OpenAI वापरण्यास सांगते.
- `api_key`, ही Azure पोर्टलमध्ये सापडलेली तुमची API की आहे.
- `api_version`, ही तुम्हाला वापरायची असलेली API ची आवृत्ती आहे. लेखनाच्या वेळी, नवीनतम आवृत्ती `2023-05-15` आहे.
- `api_base`, हा API चा एंडपॉइंट आहे. तुम्ही तुमच्या API कीच्या शेजारी Azure पोर्टलमध्ये तो शोधू शकता.

> [!NOTE] > `os.getenv` ही एक फंक्शन आहे जी पर्यावरणीय व्हेरिएबल्स वाचते. तुम्ही `OPENAI_API_KEY` आणि `API_BASE` सारख्या पर्यावरणीय व्हेरिएबल्स वाचण्यासाठी याचा वापर करू शकता. तुमच्या टर्मिनलमध्ये किंवा `dotenv` सारख्या लायब्ररीचा वापर करून ही पर्यावरणीय व्हेरिएबल्स सेट करा.

## टेक्स्ट जनरेट करा

टेक्स्ट जनरेट करण्याचा मार्ग म्हणजे `Completion` वर्ग वापरणे. येथे एक उदाहरण आहे:

```python
prompt = "Complete the following: Once upon a time there was a"

completion = openai.Completion.create(model="davinci-002", prompt=prompt)
print(completion.choices[0].text)
```

वरील कोडमध्ये, आम्ही एक कंप्लीशन ऑब्जेक्ट तयार करतो आणि आम्हाला वापरायचे मॉडेल आणि प्रॉम्प्ट पास करतो. नंतर आम्ही तयार केलेला टेक्स्ट प्रिंट करतो.

### चॅट कंप्लीशन्स

आतापर्यंत, तुम्ही पाहिले आहे की आम्ही टेक्स्ट जनरेट करण्यासाठी `Completion` वापरत आहोत. पण एक `ChatCompletion` नावाचा दुसरा वर्ग आहे जो चॅटबॉट्ससाठी अधिक योग्य आहे. त्याचा वापर करण्याचे उदाहरण येथे आहे:

```python
import openai

openai.api_key = "sk-..."

completion = openai.ChatCompletion.create(model="gpt-3.5-turbo", messages=[{"role": "user", "content": "Hello world"}])
print(completion.choices[0].message.content)
```

या कार्यक्षमतेबद्दल अधिक माहिती आगामी अध्यायात.

## व्यायाम - तुमचा पहिला टेक्स्ट जनरेशन अॅप

आता आपण openai सेट अप आणि कॉन्फिगर कसे करायचे ते शिकलो आहोत, आता तुमचा पहिला टेक्स्ट जनरेशन अॅप तयार करण्याची वेळ आली आहे. तुमचा अॅप तयार करण्यासाठी, खालील चरणांचे अनुसरण करा:

1. एक वर्च्युअल एन्व्हायर्नमेंट तयार करा आणि openai इंस्टॉल करा:

   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install openai
   ```

   > [!NOTE]
   > जर तुम्ही Windows वापरत असाल तर `source venv/bin/activate` ऐवजी `venv\Scripts\activate` टाइप करा.

   > [!NOTE]
   > तुमची Azure OpenAI की शोधण्यासाठी [https://portal.azure.com/](https://portal.azure.com/?WT.mc_id=academic-105485-koreyst) वर जा आणि `Open AI` शोधा आणि `Open AI resource` निवडा आणि नंतर `Keys and Endpoint` निवडा आणि `Key 1` मूल्य कॉपी करा.

1. एक _app.py_ फाइल तयार करा आणि त्यामध्ये खालील कोड द्या:

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
   > जर तुम्ही Azure OpenAI वापरत असाल, तर तुम्हाला `api_type` `azure` वर सेट करणे आवश्यक आहे आणि `api_key` तुमच्या Azure OpenAI की वर सेट करणे आवश्यक आहे.

   तुम्हाला खालीलप्रमाणे आउटपुट दिसेल:

   ```output
    very unhappy _____.

   Once upon a time there was a very unhappy mermaid.
   ```

## वेगवेगळ्या प्रकारचे प्रॉम्प्ट्स, वेगवेगळ्या गोष्टींसाठी

आता तुम्ही पाहिले आहे की प्रॉम्प्ट वापरून टेक्स्ट कसे जनरेट करायचे. तुमच्याकडे एक प्रोग्राम देखील चालू आहे ज्यामध्ये तुम्ही बदल करू शकता आणि वेगवेगळ्या प्रकारचा टेक्स्ट जनरेट करू शकता.

प्रॉम्प्ट्स सर्व प्रकारच्या कार्यांसाठी वापरले जाऊ शकतात. उदाहरणार्थ:

- **टेक्स्ट तयार करा**. उदाहरणार्थ, तुम्ही कविता, क्विझसाठी प्रश्न इत्यादी तयार करू शकता.
- **माहिती शोधा**. तुम्ही प्रॉम्प्ट्स वापरून माहिती शोधू शकता, जसे की 'वेब डेव्हलपमेंटमध्ये CORS म्हणजे काय?'.
- **कोड तयार करा**. तुम्ही कोड तयार करण्यासाठी प्रॉम्प्ट्स वापरू शकता, उदाहरणार्थ ईमेल्स सत्यापित करण्यासाठी वापरले जाणारे रेग्युलर एक्सप्रेशन विकसित करणे किंवा संपूर्ण प्रोग्राम तयार करणे, जसे की वेब अॅप?

## एक अधिक व्यावहारिक उपयोग: रेसिपी जनरेटर

कल्पना करा की तुमच्याकडे घरी काही साहित्य आहे आणि तुम्हाला काहीतरी बनवायचे आहे. त्यासाठी तुम्हाला रेसिपीची आवश्यकता आहे. रेसिपी शोधण्याचा एक मार्ग म्हणजे सर्च इंजिन वापरणे किंवा तुम्ही LLM वापरू शकता.

तुम्ही खालीलप्रमाणे प्रॉम्प्ट लिहू शकता:

> "मला खालील साहित्य असलेल्या डिशसाठी 5 रेसिपी दाखवा: चिकन, बटाटे आणि गाजर. प्रत्येक रेसिपीसाठी, वापरलेली सर्व सामग्री सूचीबद्ध करा"

वरील प्रॉम्प्ट दिल्यानंतर, तुम्हाला खालीलप्रमाणे प्रतिसाद मिळू शकतो:

```output
1. Roasted Chicken and Vegetables:
Ingredients:
- 4 chicken thighs
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 2 tablespoons olive oil
- 2 cloves garlic, minced
- 1 teaspoon dried thyme
- 1 teaspoon dried oregano
- Salt and pepper, to taste

2. Chicken and Potato Stew:
Ingredients:
- 2 tablespoons olive oil
- 1 onion, diced
- 2 cloves garlic, minced
- 2 chicken breasts, cut into cubes
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 1 teaspoon dried oregano
- 1 teaspoon dried thyme
- 1 cup chicken broth
- Salt and pepper, to taste

3. Chicken and Potato Bake:
Ingredients:
- 2 tablespoons olive oil
- 2 chicken breasts, cut into cubes
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 1 onion, diced
- 2 cloves garlic, minced
- 1 teaspoon dried oregano
- 1 teaspoon dried thyme
- 1 cup chicken broth
- Salt and pepper, to taste

4. Chicken and Potato Soup:
Ingredients:
- 2 tablespoons olive oil
- 1 onion, diced
- 2 cloves garlic, minced
- 2 chicken breasts, cut into cubes
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 1 teaspoon dried oregano
- 1 teaspoon dried thyme
- 4 cups chicken broth
- Salt and pepper, to taste

5. Chicken and Potato Hash:
Ingredients:
- 2 tablespoons olive oil
- 2 chicken breasts, cut into cubes
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 1 onion, diced
- 2 cloves garlic, minced
- 1 teaspoon dried oregano
```

हे परिणाम उत्कृष्ट आहेत, मला काय बनवायचे आहे ते माहित आहे. या टप्प्यावर, उपयुक्त सुधारणा काय असू शकतात:

- मला आवडत नाही किंवा ज्यामुळे मला अॅलर्जी आहे अशा साहित्यांना फिल्टर करणे.
- खरेदी यादी तयार करणे, जर माझ्याकडे सर्व साहित्य घरी नसेल तर.

वरील प्रकरणांसाठी, चला एक अतिरिक्त प्रॉम्प्ट जोडूया:

> "कृपया लसूण असलेल्या रेसिपी काढा कारण मला अॅलर्जी आहे आणि त्याऐवजी काहीतरी बदला. तसेच, कृपया रेसिपीसाठी खरेदी यादी तयार करा, विचार करा की माझ्याकडे आधीच चिकन, बटाटे आणि गाजर आहेत."

आता तुम्हाला एक नवीन परिणाम मिळाला आहे, म्हणजे:

```output
1. Roasted Chicken and Vegetables:
Ingredients:
- 4 chicken thighs
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 2 tablespoons olive oil
- 1 teaspoon dried thyme
- 1 teaspoon dried oregano
- Salt and pepper, to taste

2. Chicken and Potato Stew:
Ingredients:
- 2 tablespoons olive oil
- 1 onion, diced
- 2 chicken breasts, cut into cubes
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 1 teaspoon dried oregano
- 1 teaspoon dried thyme
- 1 cup chicken broth
- Salt and pepper, to taste

3. Chicken and Potato Bake:
Ingredients:
- 2 tablespoons olive oil
- 2 chicken breasts, cut into cubes
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 1 onion, diced
- 1 teaspoon dried oregano
- 1 teaspoon dried thyme
- 1 cup chicken broth
- Salt and pepper, to taste

4. Chicken and Potato Soup:
Ingredients:
- 2 tablespoons olive oil
- 1 onion, diced
- 2 chicken breasts, cut into cubes
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 1 teaspoon dried oregano
- 1 teaspoon dried thyme
- 4 cups chicken broth
- Salt and pepper, to taste

5. Chicken and Potato Hash:
Ingredients:
- 2 tablespoons olive oil
- 2 chicken breasts, cut into cubes
- 2 potatoes, cut into cubes
- 2 carrots, cut into cubes
- 1 onion, diced
- 1 teaspoon dried oregano

Shopping List:
- Olive oil
- Onion
- Thyme
- Oregano
- Salt
- Pepper
```

तुमच्या पाच रेसिपी आहेत, त्यामध्ये लसूणचा उल्लेख नाही आणि तुमच्याकडे घरी आधीच असलेल्या गोष्टी विचारात घेऊन तुम्हाला खरेदी यादी देखील मिळाली आहे.

## व्यायाम - रेसिपी जनरेटर तयार करा

आता आपण एक परिस्थिती खेळून पाहिली आहे, चला प्रदर्शित परिस्थितीशी जुळणारा कोड लिहूया. असे करण्यासाठी, खालील चरणांचे अनुसरण करा:

1. विद्यमान _app.py_ फाइल प्रारंभ बिंदू म्हणून वापरा
1. `prompt` व्हेरिएबल शोधा आणि त्याचा कोड खालीलप्रमाणे बदला:

   ```python
   prompt = "Show me 5 recipes for a dish with the following ingredients: chicken, potatoes, and carrots. Per recipe, list all the ingredients used"
   ```

   जर तुम्ही आता कोड चालवला, तर तुम्हाला खालीलप्रमाणे आउटपुट दिसेल:

   ```output
   -Chicken Stew with Potatoes and Carrots: 3 tablespoons oil, 1 onion, chopped, 2 cloves garlic, minced, 1 carrot, peeled and chopped, 1 potato, peeled and chopped, 1 bay leaf, 1 thyme sprig, 1/2 teaspoon salt, 1/4 teaspoon black pepper, 1 1/2 cups chicken broth, 1/2 cup dry white wine, 2 tablespoons chopped fresh parsley, 2 tablespoons unsalted butter, 1 1/2 pounds boneless, skinless chicken thighs, cut into 1-inch pieces
   -Oven-Roasted Chicken with Potatoes and Carrots: 3 tablespoons extra-virgin olive oil, 1 tablespoon Dijon mustard, 1 tablespoon chopped fresh rosemary, 1 tablespoon chopped fresh thyme, 4 cloves garlic, minced, 1 1/2 pounds small red potatoes, quartered, 1 1/2 pounds carrots, quartered lengthwise, 1/2 teaspoon salt, 1/4 teaspoon black pepper, 1 (4-pound) whole chicken
   -Chicken, Potato, and Carrot Casserole: cooking spray, 1 large onion, chopped, 2 cloves garlic, minced, 1 carrot, peeled and shredded, 1 potato, peeled and shredded, 1/2 teaspoon dried thyme leaves, 1/4 teaspoon salt, 1/4 teaspoon black pepper, 2 cups fat-free, low-sodium chicken broth, 1 cup frozen peas, 1/4 cup all-purpose flour, 1 cup 2% reduced-fat milk, 1/4 cup grated Parmesan cheese

   -One Pot Chicken and Potato Dinner: 2 tablespoons olive oil, 1 pound boneless, skinless chicken thighs, cut into 1-inch pieces, 1 large onion, chopped, 3 cloves garlic, minced, 1 carrot, peeled and chopped, 1 potato, peeled and chopped, 1 bay leaf, 1 thyme sprig, 1/2 teaspoon salt, 1/4 teaspoon black pepper, 2 cups chicken broth, 1/2 cup dry white wine

   -Chicken, Potato, and Carrot Curry: 1 tablespoon vegetable oil, 1 large onion, chopped, 2 cloves garlic, minced, 1 carrot, peeled and chopped, 1 potato, peeled and chopped, 1 teaspoon ground coriander, 1 teaspoon ground cumin, 1/2 teaspoon ground turmeric, 1/2 teaspoon ground ginger, 1/4 teaspoon cayenne pepper, 2 cups chicken broth, 1/2 cup dry white wine, 1 (15-ounce) can chickpeas, drained and rinsed, 1/2 cup raisins, 1/2 cup chopped fresh cilantro
   ```

   > लक्षात ठेवा, तुमचा LLM nondeterministic आहे, त्यामुळे तुम्हाला प्रत्येक वेळी प्रोग्राम चालवताना वेगवेगळे परिणाम मिळू शकतात.

   छान, चला पाहूया की आपण गोष्टी कशा सुधारू शकतो. गोष्टी सुधारण्यासाठी, आम्हाला खात्री करायची आहे की कोड लवचिक आहे, त्यामुळे साहित्य आणि रेसिपींची संख्या सुधारली जाऊ शकते आणि बदलली जाऊ शकते.

1. चला कोड खालीलप्रमाणे बदलूया:

   ```python
   no_recipes = input("No of recipes (for example, 5): ")

   ingredients = input("List of ingredients (for example, chicken, potatoes, and carrots): ")

   # interpolate the number of recipes into the prompt an ingredients
   prompt = f"Show me {no_recipes} recipes for a dish with the following ingredients: {ingredients}. Per recipe, list all the ingredients used"
   ```

   कोड चाचणीसाठी चालवणे, असे दिसू शकते:

   ```output
   No of recipes (for example, 5): 3
   List of ingredients (for example, chicken, potatoes, and carrots): milk,strawberries

   -Strawberry milk shake: milk, strawberries, sugar, vanilla extract, ice cubes
   -Strawberry shortcake: milk, flour, baking powder, sugar, salt, unsalted butter, strawberries, whipped cream
   -Strawberry milk: milk, strawberries, sugar, vanilla extract
   ```

### फिल्टर आणि खरेदी यादी जोडून सुधारणा करा

आता आमच्याकडे रेसिपी तयार करण्यास सक्षम असलेला कार्यरत अॅप आहे आणि तो लवचिक आहे कारण तो वापरकर्त्याच्या इनपुटवर अवलंबून आहे, रेसिपींच्या संख्येवर तसेच वापरलेल्या साहित्यावर.

याला पुढे सुधारण्यासाठी, आम्हाला खालील गोष्टी जोडायच्या आहेत:

- **साहित्य फिल्टर करा**. आम्हाला असे साहित्य फिल्टर करायचे आहे जे आम्हाला आवडत नाही किंवा ज्यामुळे आम्हाला अॅलर्जी आहे. ही बदल घडवून आणण्यासाठी, आम्ही आमच्या विद्यमान प्रॉम्प्टमध्ये संपादन करू शकतो आणि त्याच्या शेवटी फिल्टर अटी जोडू शकतो:

  ```python
  filter = input("Filter (for example, vegetarian, vegan, or gluten-free): ")

  prompt = f"Show me {no_recipes} recipes for a dish with the following ingredients: {ingredients}. Per recipe, list all the ingredients used, no {filter}"
  ```

  वरीलमध्ये, आम्ही प्रॉम्प्टच्या शेवटी `{filter}` जोडतो आणि आम्ही वापरकर्त्याकडून फिल्टर मूल्य देखील कॅप्चर करतो.

  प्रोग्राम चालवण्याचा एक उदाहरण इनपुट आता असे दिसू शकतो:

  ```output
  No of recipes (for example, 5): 3
  List of ingredients (for example, chicken, potatoes, and carrots): onion,milk
  Filter (for example, vegetarian, vegan, or gluten-free): no milk

  1. French Onion Soup

  Ingredients:

  -1 large onion, sliced
  -3 cups beef broth
  -1 cup milk
  -6 slices french bread
  -1/4 cup shredded Parmesan cheese
  -1 tablespoon butter
  -1 teaspoon dried thyme
  -1/4 teaspoon salt
  -1/4 teaspoon black pepper

  Instructions:

  1. In a large pot, sauté onions in butter until golden brown.
  2. Add beef broth, milk, thyme, salt, and pepper. Bring to a boil.
  3. Reduce heat and simmer for 10 minutes.
  4. Place french bread slices on soup bowls.
  5. Ladle soup over bread.
  6. Sprinkle with Parmesan cheese.

  2. Onion and Potato Soup

  Ingredients:

  -1 large onion, chopped
  -2 cups potatoes, diced
  -3 cups vegetable broth
  -1 cup milk
  -1/4 teaspoon black pepper

  Instructions:

  1. In a large pot, sauté onions in butter until golden brown.
  2. Add potatoes, vegetable broth, milk, and pepper. Bring to a boil.
  3. Reduce heat and simmer for 10 minutes.
  4. Serve hot.

  3. Creamy Onion Soup

  Ingredients:

  -1 large onion, chopped
  -3 cups vegetable broth
  -1 cup milk
  -1/4 teaspoon black pepper
  -1/4 cup all-purpose flour
  -1/2 cup shredded Parmesan cheese

  Instructions:

  1. In a large pot, sauté onions in butter until golden brown.
  2. Add vegetable broth, milk, and pepper. Bring to a boil.
  3. Reduce heat and simmer for 10 minutes.
  4. In a small bowl, whisk together flour and Parmesan cheese until smooth.
  5. Add to soup and simmer for an additional 5 minutes, or until soup has thickened.
  ```

  तुम्ही पाहू शकता, दूध असलेल्या कोणत्याही रेसिपी फिल्टर केल्या
कोडमध्ये पहिल्या प्रॉम्प्टमधून परिणाम प्रिंट करणारा भाग शोधा आणि खालील कोड जोडा:

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

खालील गोष्टी लक्षात घ्या:

1. आम्ही नवीन प्रॉम्प्ट तयार करत आहोत, ज्यामध्ये पहिल्या प्रॉम्प्टमधून मिळालेला परिणाम नवीन प्रॉम्प्टमध्ये जोडत आहोत:

     ```python
     new_prompt = f"{old_prompt_result} {prompt}"
     ```

1. आम्ही नवीन विनंती करतो, पण पहिल्या प्रॉम्प्टमध्ये विचारलेल्या टोकन्सच्या संख्येचा विचार करून, यावेळी `max_tokens` 1200 म्हणतो.

     ```python
     completion = openai.Completion.create(engine=deployment_name, prompt=new_prompt, max_tokens=1200)
     ```

   हा कोड वापरून पाहिल्यावर, आम्हाला खालील आउटपुट मिळते:

     ```output
     No of recipes (for example, 5): 2
     List of ingredients (for example, chicken, potatoes, and carrots): apple,flour
     Filter (for example, vegetarian, vegan, or gluten-free): sugar


     -Apple and flour pancakes: 1 cup flour, 1/2 tsp baking powder, 1/2 tsp baking soda, 1/4 tsp salt, 1 tbsp sugar, 1 egg, 1 cup buttermilk or sour milk, 1/4 cup melted butter, 1 Granny Smith apple, peeled and grated
     -Apple fritters: 1-1/2 cups flour, 1 tsp baking powder, 1/4 tsp salt, 1/4 tsp baking soda, 1/4 tsp nutmeg, 1/4 tsp cinnamon, 1/4 tsp allspice, 1/4 cup sugar, 1/4 cup vegetable shortening, 1/4 cup milk, 1 egg, 2 cups shredded, peeled apples
     Shopping list:
     -Flour, baking powder, baking soda, salt, sugar, egg, buttermilk, butter, apple, nutmeg, cinnamon, allspice
     ```

## तुमची सेटअप सुधारित करा

आत्तापर्यंत आपल्याकडे कार्यरत कोड आहे, पण काही सुधारणा केल्यास गोष्टी अधिक चांगल्या होऊ शकतात. आपण करावयाच्या काही गोष्टी:

- **गुपिते कोडपासून वेगळी करा**, जसे की API की. गुपिते कोडमध्ये असू नयेत आणि सुरक्षित ठिकाणी संग्रहित केली पाहिजेत. गुपिते कोडपासून वेगळी करण्यासाठी, आपण पर्यावरणीय व्हेरिएबल्स आणि `python-dotenv` सारख्या लायब्ररी वापरू शकतो, ज्यामुळे ती फाइलमधून लोड करता येतील. कोडमध्ये हे कसे दिसेल:

  1. `.env` फाइल तयार करा, ज्यामध्ये खालील सामग्री असेल:

     ```bash
     OPENAI_API_KEY=sk-...
     ```

   > लक्षात ठेवा, Azure साठी, तुम्हाला खालील पर्यावरणीय व्हेरिएबल्स सेट करणे आवश्यक आहे:

     ```bash
     OPENAI_API_TYPE=azure
     OPENAI_API_VERSION=2023-05-15
     OPENAI_API_BASE=<replace>
     ```

   कोडमध्ये, तुम्ही पर्यावरणीय व्हेरिएबल्स खालीलप्रमाणे लोड करू शकता:

     ```python
     from dotenv import load_dotenv

     load_dotenv()

     openai.api_key = os.environ["OPENAI_API_KEY"]
     ```

- **टोकन लांबीबद्दल एक शब्द**. आपल्याला आवश्यक असलेल्या मजकूरासाठी किती टोकन्स लागतील याचा विचार करायला हवा. टोकन्ससाठी पैसे लागतात, त्यामुळे शक्य असल्यास, आपण वापरलेल्या टोकन्सची संख्या कमी करण्याचा प्रयत्न करावा. उदाहरणार्थ, आपण प्रॉम्प्ट कसे मांडतो यावर टोकन्स कमी वापरता येतील का?

  वापरलेले टोकन्स बदलण्यासाठी, तुम्ही `max_tokens` पॅरामीटर वापरू शकता. उदाहरणार्थ, जर तुम्हाला 100 टोकन्स वापरायचे असतील, तर तुम्ही असे करू शकता:

  ```python
  completion = client.chat.completions.create(model=deployment, messages=messages, max_tokens=100)
  ```

- **तापमानासह प्रयोग करणे**. तापमान ही एक गोष्ट आहे जी आपण अद्याप उल्लेख केलेली नाही, पण आपल्या प्रोग्रामच्या कार्यक्षमतेसाठी महत्त्वाची आहे. तापमानाचे मूल्य जास्त असल्यास आउटपुट अधिक अनियमित होईल. उलट, तापमानाचे मूल्य कमी असल्यास आउटपुट अधिक अंदाजे असेल. विचार करा की तुम्हाला आउटपुटमध्ये विविधता हवी आहे की नाही.

  तापमान बदलण्यासाठी, तुम्ही `temperature` पॅरामीटर वापरू शकता. उदाहरणार्थ, जर तुम्हाला 0.5 तापमान वापरायचे असेल, तर तुम्ही असे करू शकता:

  ```python
  completion = client.chat.completions.create(model=deployment, messages=messages, temperature=0.5)
  ```

  > लक्षात ठेवा, 1.0 च्या जवळ असलेले मूल्य आउटपुट अधिक विविध बनवते.

## असाइनमेंट

या असाइनमेंटसाठी, तुम्ही काय तयार करायचे ते निवडू शकता.

काही सुचवण्या येथे आहेत:

- रेसिपी जनरेटर अ‍ॅप अधिक सुधारित करा. तापमानाच्या मूल्यांशी खेळा आणि प्रॉम्प्ट्ससह प्रयोग करा, तुम्ही काय तयार करू शकता ते पाहा.
- "स्टडी बडी" तयार करा. हे अ‍ॅप एखाद्या विषयाबद्दल प्रश्नांची उत्तरे देऊ शकेल, उदाहरणार्थ Python. तुम्ही असे प्रॉम्प्ट्स देऊ शकता, "Python मधील एखादा विशिष्ट विषय काय आहे?", किंवा तुम्ही असे प्रॉम्प्ट देऊ शकता, "मला एखाद्या विशिष्ट विषयासाठी कोड दाखवा" इत्यादी.
- इतिहास बॉट, इतिहास जिवंत करा, बॉटला एखाद्या ऐतिहासिक पात्राची भूमिका बजावण्याचे निर्देश द्या आणि त्याच्या जीवन आणि काळाबद्दल प्रश्न विचारा.

## समाधान

### स्टडी बडी

खाली एक स्टार्टर प्रॉम्प्ट आहे, पाहा तुम्ही ते कसे वापरू शकता आणि तुमच्या आवडीनुसार कसे बदलू शकता.

```text
- "You're an expert on the Python language

    Suggest a beginner lesson for Python in the following format:

    Format:
    - concepts:
    - brief explanation of the lesson:
    - exercise in code with solutions"
```

### इतिहास बॉट

येथे काही प्रॉम्प्ट्स आहेत जे तुम्ही वापरू शकता:

```text
- "You are Abe Lincoln, tell me about yourself in 3 sentences, and respond using grammar and words like Abe would have used"
- "You are Abe Lincoln, respond using grammar and words like Abe would have used:

   Tell me about your greatest accomplishments, in 300 words"
```

## ज्ञान तपासणी

तापमान संकल्पना काय करते?

1. आउटपुट किती अनियमित आहे हे नियंत्रित करते.
1. प्रतिसाद किती मोठा आहे हे नियंत्रित करते.
1. वापरलेले टोकन्स किती आहेत हे नियंत्रित करते.

## 🚀 आव्हान

असाइनमेंटवर काम करताना, तापमान बदलण्याचा प्रयत्न करा, 0, 0.5, आणि 1 सेट करण्याचा प्रयत्न करा. लक्षात ठेवा की 0 सर्वात कमी विविध आहे आणि 1 सर्वात जास्त आहे. तुमच्या अ‍ॅपसाठी कोणते मूल्य सर्वात चांगले कार्य करते?

## उत्तम काम! तुमचे शिक्षण सुरू ठेवा

हा धडा पूर्ण केल्यानंतर, आमच्या [Generative AI Learning collection](https://aka.ms/genai-collection?WT.mc_id=academic-105485-koreyst) वर जा, जेणेकरून तुम्ही तुमचे Generative AI ज्ञान अधिक वाढवू शकता!

धडा 7 वर जा, जिथे आपण [चॅट अ‍ॅप्लिकेशन्स तयार करणे](../07-building-chat-applications/README.md?WT.mc_id=academic-105485-koreyst) पाहणार आहोत!

---

**अस्वीकरण**:  
हा दस्तऐवज AI भाषांतर सेवा [Co-op Translator](https://github.com/Azure/co-op-translator) वापरून भाषांतरित करण्यात आला आहे. आम्ही अचूकतेसाठी प्रयत्नशील असलो तरी, कृपयास लक्षात ठेवा की स्वयंचलित भाषांतरे त्रुटी किंवा अचूकतेच्या अभावाने युक्त असू शकतात. मूळ भाषेतील दस्तऐवज हा अधिकृत स्रोत मानला जावा. महत्त्वाच्या माहितीसाठी, व्यावसायिक मानवी भाषांतराची शिफारस केली जाते. या भाषांतराचा वापर करून निर्माण झालेल्या कोणत्याही गैरसमज किंवा चुकीच्या अर्थासाठी आम्ही जबाबदार नाही.