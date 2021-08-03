# Flutter_Voice_Chatbot
## Explanation of IOT and software development Department task:
### - Build an Android application by flutter for voice chatbot.

## Dependencies
```
  cupertino_icons: ^0.1.3
  speech_to_text: ^4.2.2
  highlight_text: ^1.1.0
  avatar_glow: ^1.2.0
```

## IBM Cloud services

```
<!--Watson Assistant service credentials-->
    <string name="assistant_apikey">w7tshqK-n2Srh8ow3ZtrmjkJ7skPmhnehpebATzY7JIB</string>
    <string name="assistant_url">https://api.eu-de.assistant.watson.cloud.ibm.com/instances/577cf4c6-bc6d-45f2-8f67-817b73ac8329</string>


    <!--Watson Speech To Text(STT) service credentials-->
    <string name="STT_apikey">Y3aLQIVb9ZB2Yi6jJ9ffUzkaI8DWyOGeUzdeFsx0s16b</string>
    <string name="STT_url">https://api.us-south.speech-to-text.watson.cloud.ibm.com/instances/3b2812fa-41fc-4d74-8154-880474bf9d90</string>


    <!--Watson Text To Speech(TTS) service credentials-->
    <string name="TTS_apikey">D1Qd_dD1uvRjtLxOnY6YWj7RFP_tSsv6pDGQONE0XEZ5</string>
    <string name="TTS_url">https://api.au-syd.text-to-speech.watson.cloud.ibm.com/instances/51d8e3fd-7511-46c3-b4ac-79c3a6986747</string>

```

## Watson Speech to Text Methods
```
 private class MicrophoneRecognizeDelegate extends BaseRecognizeCallback {
        @Override
        public void onTranscription(SpeechRecognitionResults speechResults) {
            if (speechResults.getResults() != null && !speechResults.getResults().isEmpty()) {
                String text = speechResults.getResults().get(0).getAlternatives().get(0).getTranscript();
                showMicText(text);
            }
        }
```
