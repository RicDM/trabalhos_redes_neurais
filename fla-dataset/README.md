# FLA-Dataset: A Database of Four Location-Based Audio Commands in Brazilian Portuguese

**FLA-Dataset** is a wake word dataset in Brazilian Portuguese designed to train and evaluate keyword spotting and voice command recognition systems. It is suitable for applications such as virtual assistants, embedded systems, and robotics.

## Dataset Structure

The dataset is organized into four main folders, one for each activation word:

- `direita/` (right)
- `esquerda/` (left)
- `frente/` (forward)
- `pare/` (stop)

Each folder contains `.wav` audio files sampled at **16 kHz**, with recordings of different speakers pronouncing the corresponding word.

## File Naming Convention

Files follow the naming pattern:

```
<word>_s<speaker_id>_a<sample_id>.wav
```

- `sXXX` indicates the speaker ID  
- `aYYY` indicates the audio sample number for that speaker

## Speakers

FLA-Dataset includes recordings from **30 speakers**, with the following gender distribution:
- **10 female** (IDs: s000 to s009)
- **20 male** (IDs: s010 to s029)

This speaker diversity supports more robust and generalizable models.

## Statistics

The dataset contains a total of **2,329 audio samples**, distributed as follows:

| Word      | Number of Samples |
|-----------|-------------------|
| direita   | 624               |
| esquerda  | 514               |
| frente    | 597               |
| pare      | 594               |

- **Total Duration**: 40.78 minutes  
- **Average Duration per Audio**: 1.05 seconds

## Audio Specifications

- **Format**: WAV  
- **Sample Rate**: 16 kHz  
- **Type**: Isolated words  
- **Language**: Brazilian Portuguese

## Potential Applications

- Wake word detection  
- Voice command recognition  
- Embedded systems and voice-based interfaces in Portuguese
