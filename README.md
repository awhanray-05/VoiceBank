# 🎙️ VoiceBank

**VoiceBank** is a voice-driven Android application designed to provide secure and seamless user interactions using speech commands. It integrates biometric authentication, speech-to-text, text-to-speech, and a locally loaded voice model (**FRILL**) for a fully interactive voice banking experience.

---

## ✨ Features

- 🎤 **Voice Input with Speech Recognition**  
  Uses Android's `SpeechRecognizer` (via `VoiceToTextParser`) for converting voice commands into text.

- 🔊 **Text-to-Speech Output**  
  Provides audio responses using `TextToSpeechHelper`, enhancing accessibility and interaction quality.

- 🧠 **Local FRILL Model Integration**  
  Loads a custom `FRILLModel` for intelligent voice interaction on-device.

- 🔐 **Biometric Authentication**  
  Secures app access with fingerprint or face unlock via `BiometricPromptManager`.

- 🔁 **MVVM Architecture**  
  Clean separation of logic using ViewModel, Repository, and Factory classes (`AuthViewModel`, `AuthRepository`, etc.).

- 🎨 **Jetpack Compose UI**  
  Modern, declarative UI powered by Jetpack Compose and a custom theme (`VoiceBankTheme`).

- 📱 **Permission Handling**  
  Dynamically requests and manages microphone permissions using `ActivityResultContracts`.

---

## 🧱 Tech Stack

| Layer         | Technology          |
|---------------|---------------------|
| Language       | Kotlin              |
| UI             | Jetpack Compose     |
| Architecture   | MVVM                |
| Voice Input    | SpeechRecognizer    |
| Text-to-Speech | Android TTS         |
| Security       | BiometricPrompt API |
| AI Model       | FRILL (on-device)   |
| Auth Backend   | FirebaseAuth        |

---

## 📂 Project Structure Overview

com.skye.voicebank
│
├── MainActivity.kt # Entry point of the app
├── viewmodels/
│ ├── AuthViewModel.kt
│ ├── AuthViewModelFactory.kt
│ ├── AuthRepository.kt
│ └── FirebaseAuthRepository.kt
├── utils/
│ ├── FRILLModel.kt # Loads the on-device voice model
│ ├── TextToSpeechHelper.kt # TTS utility
│ └── VoiceToTextParser.kt # STT utility
├── screens/
│ └── NavigationGraph.kt # Navigation host setup
└── ui/theme/
└── VoiceBankTheme.kt # App theme


---

## 🔐 Required Permissions

- `RECORD_AUDIO` – Required to capture voice input
- `USE_BIOMETRIC` – Required for fingerprint or face unlock (handled implicitly)

---

## 🚀 Getting Started

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-username/voicebank.git
   cd voicebank
