BHAVNA AI — शुरुआती Android प्रोजेक्ट
====================================

क्या मिलता है?
- Holographic universe शैली का इंटरफेस
- हिंदी में टेक्स्ट चैट
- Android के उपलब्ध speech engine से जवाब बोलने की कोशिश
- Gemini Cloud AI के लिए वैकल्पिक API key
- बिना इंटरनेट का बहुत साधारण Local basic mode

महत्वपूर्ण सीमाएँ:
1. यह शुरुआती MVP है, ChatGPT जितना पूरा या असीमित AI नहीं।
2. Local basic mode असली लोकल LLM नहीं है; वह सीमित नियम-आधारित जवाब देता है।
3. Gemini API की मुफ्त सीमा/मॉडल उपलब्धता बदल सकती है। मुफ्त या अनलिमिटेड होने की गारंटी नहीं।
4. API key को APK में hard-code न करें। इस डेमो में key ऐप के स्थानीय storage में रखी जाती है, फिर भी साझा डिवाइस पर सावधान रहें।
5. WebView में बोलकर लिखने की सुविधा हर Android डिवाइस पर काम नहीं करती; न चले तो कीबोर्ड का माइक्रोफोन उपयोग करें।

फोन पर APK बनाने के स्टेप:
1. ZIP को extract करें।
2. AndroidIDE केवल आधिकारिक स्रोत से इंस्टॉल करें:
   https://docs.androidide.com/user/installation.html
3. AndroidIDE खोलें और पहली बार build tools setup पूरा करें। लगभग 4GB खाली जगह और Wi-Fi रखें।
4. Extract किए हुए BhavnaAI फ़ोल्डर को AndroidIDE में Open existing project से खोलें।
5. Gradle sync पूरा होने दें। पहली बार काफी समय लग सकता है।
6. Quick Run / Run दबाएँ। Debug APK बनेगा और इंस्टॉल करने का विकल्प आएगा।
7. अगर Gradle/SDK संस्करण की त्रुटि आए तो AndroidIDE के build output का screenshot भेजें।

Gemini API key:
1. https://aistudio.google.com/ पर अपने Google खाते से जाएँ।
2. API key बनाने का विकल्प देखें।
3. ऐप में Cloud API key बॉक्स में key डालें और सेव दबाएँ।
4. Cloud AI मोड चुनकर सवाल भेजें।
5. API key किसी के साथ साझा न करें। मुफ्त सीमा और उपलब्ध मॉडल खाते/क्षेत्र के अनुसार बदल सकते हैं।

फ़ोल्डर संरचना:
BhavnaAI/
  settings.gradle
  build.gradle
  gradle.properties
  app/
    build.gradle
    src/main/AndroidManifest.xml
    src/main/java/com/bhavna/ai/MainActivity.java
    src/main/assets/index.html
