# New App

New App is an application that allows users to translate and voice over any video from a given link with high quality.

## User Journey

1. **Access the App**: The user opens the New App.

2. **Sign In**:
   - The app displays a "Sign in with ZAPT" message and provides options to sign in using email (magic link) or social providers (Google, Facebook, Apple).
   - The user signs in, and the app updates to show the main functionality without needing to refresh the page.

3. **Provide Video Link**:
   - On the home page, the user sees a form to input a video link.
   - The user enters the URL of the video they wish to translate.

4. **Select Target Language**:
   - The user chooses the language for translation from a dropdown menu.

5. **Submit the Request**:
   - The user clicks the "Translate and Voiceover" button to submit the request.
   - The button is disabled to prevent multiple submissions.
   - A loading state indicates that the video is being processed.

6. **Processing**:
   - The backend processes the video:
     - Downloads the video.
     - Extracts the audio and transcribes it.
     - Translates the transcription into the target language.
     - Uses text-to-speech to generate audio in the target language.
     - Combines the new audio with the original video.

7. **Receive Translated Video**:
   - Once processing is complete, the user can view the translated and voice-overed video directly in the app.
   - The user can also download the video if they wish.

8. **Sign Out**:
   - The user can sign out by clicking the "Sign Out" button.
   - The app updates without needing to refresh the page.

## External APIs Used

- **Video Processing API**: The app uses an external API to process videos, including downloading, transcribing, translating, and generating voiceovers.
- **Speech Recognition API**: Used to transcribe the original audio into text.
- **Translation API**: Used to translate the transcribed text into the target language.
- **Text-to-Speech API**: Used to generate the voiceover in the target language.

## Environment Variables Required

- `VITE_PUBLIC_SENTRY_DSN`: Your Sentry DSN for error tracking.
- `VITE_PUBLIC_APP_ENV`: The environment (e.g., development, production).
- `VITE_PUBLIC_APP_ID`: Your app ID.
- `VIDEO_API_KEY`: API key for the video processing service.
- `SPEECH_API_KEY`: API key for the speech recognition service.
- `TRANSLATION_API_KEY`: API key for the translation service.
- `TTS_API_KEY`: API key for the text-to-speech service.
