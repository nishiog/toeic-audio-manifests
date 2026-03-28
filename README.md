# toeic-audio-manifests

Structured chapter/section metadata for TOEIC® official audio files.

Each manifest JSON maps MP3 filenames to timestamped sections (question numbers, options, conversations, etc.), enabling any app to implement chapter navigation, A-B repeat, and section-based playback without modifying app binaries.

## Schema

```json
{
  "book_id": "<uuid>",
  "title": "<book title>",
  "tracks": [
    {
      "file_name": "020 T1 Part 2 Q7.mp3",
      "sections": [
        { "id": "<filename>_sec1", "label": "Question Number", "start": 0.52, "end": 1.41 },
        { "id": "<filename>_sec2", "label": "Question",        "start": 2.48, "end": 5.87 },
        { "id": "<filename>_sec3", "label": "Option A",        "start": 6.93, "end": 9.24 },
        { "id": "<filename>_sec4", "label": "Option B",        "start": 10.27, "end": 12.55 },
        { "id": "<filename>_sec5", "label": "Option C",        "start": 13.50, "end": 15.81 }
      ]
    }
  ]
}
```

## Available Manifests

| File | Description |
|------|-------------|
| [all_toeic_official_lr_12_test_1_album_1_manifest.json](manifests/all_toeic_official_lr_12_test_1_album_1_manifest.json) | TOEIC L&R 公式問題集12 Test 1 Album 1 |

## Section Labels by Part

| Part | Sections |
|------|----------|
| Part 1 | Question Number / Question / Option A / B / C / D |
| Part 2 | Question Number / Question / Option A / B / C |
| Part 3/4 会話・トーク | Introduction / Conversation 1, 2, ... (or Talk 1, 2, ...) |
| Part 3/4 設問 | Question 1, 2, 3 / (Go on) |
| Part 5/6/7 特典 | Section 1, 2, ... |
