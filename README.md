# 🧠 Dropshipping AI Research Agent

Çoklu kaynaklardan (Reddit, GitHub, YouTube, Web) otomatik araştırma yaparak dropshipping bilgisi toplayan, öğrenen ve sentezleyen AI Agent.

## 🚀 Hızlı Başlangıç

### 1. API Anahtarlarını Ayarla

```bash
cp .env.example .env
```

`.env` dosyasını açıp API anahtarlarını girin:

| Servis | Nereden Alınır | Ücretsiz mi? |
|--------|----------------|--------------|
| **Google Gemini** | [aistudio.google.com/apikey](https://aistudio.google.com/apikey) | ✅ Evet |
| **Tavily** | [tavily.com](https://tavily.com) | ✅ 1000 kredi/ay |
| **Reddit** | [reddit.com/prefs/apps](https://www.reddit.com/prefs/apps) | ✅ Evet |
| **YouTube** | [console.cloud.google.com](https://console.cloud.google.com/apis/credentials) | ✅ Günlük kota |

### 2. Bağımlılıkları Kur

```bash
pip install -r requirements.txt
```

### 3. Çalıştır

```bash
python -m uvicorn app.main:app --reload --port 8000
```

Tarayıcıda açın: **http://localhost:8000**

## 🏗️ Mimari

```
Kullanıcı → Web UI → FastAPI Backend → Orkestratör
                                          ├── Web Search Agent (Tavily)
                                          ├── Reddit Agent (PRAW)
                                          ├── GitHub Agent (REST API)
                                          ├── YouTube Agent (Data API)
                                          └── Sentezleyici (Gemini AI)
                                                    ↓
                                             ChromaDB Bilgi Tabanı
```

## ✨ Özellikler

- 🔍 **Çoklu Kaynak Araştırma** — Web, Reddit, GitHub, YouTube paralel arama
- 🧠 **Öğrenen Bilgi Tabanı** — Her araştırma ChromaDB'ye kaydedilir
- 📊 **AI Sentez** — Gemini AI ile çoklu kaynak sentezi ve Türkçe raporlama
- 🌐 **Modern Web UI** — Dark mode, gerçek zamanlı ilerleme, WebSocket
- 🎯 **Kaynak Çeşitliliği** — Tek kanala/kişiye bağlı kalmadan araştırma
