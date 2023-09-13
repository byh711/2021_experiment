# 2021 Experiment: Human-Agent Interaction in "Don't Starve Together"

## 1. Overview
This repository contains the source code and datasets used for our research project on human-agent interaction in the cooperative game "Don't Starve Together". Our research emphasizes the importance of understanding cross-cultural language differences and their effects on social cognition during interactions.

## 2. Research Paper
### Effects of Cross-Cultural Language Differences on Social Cognition during Human-Agent Interaction in Cooperative Game Environments

#### 2.1 Publication Details
- **Journal:** Computer speech & language Volume: 81 (2023) ISSN: 0885-2308
- **Authors:** Casey C. Bennett, Young-Ho Bae, Jun Hyung Yoon, Yejin Chae, Eunseo Yoon, Seeun Lee, Uijae Ryu, Benjamin Weiss
- **Link:** [ScienceDirect Paper](https://doi.org/10.1016/j.csl.2023.101521.)

#### 2.2 Abstract
A major challenge in human-robot interaction (HRI) is creating the “social fluidity” necessary for humans to perceive the interaction as life-like. During verbal interactions, for instance, the speech content itself is not the only thing that matters. Rather, things like timing, cadence, and manner of speaking are necessary to speak “like a native”, yet those attributes vary significantly by language and cultural setting. To that end, we developed a bilingual virtual avatar (Korean and English speaking) capable of autonomous speech during cooperative gameplay with a human participant in a social survival video game. We then ran a series of experiments with 60 participants (30 English speakers and 30 Korean speakers) interacting with the avatar during 30-minute game sessions. The experiments included several conditions, in which we modified the avatar's speech behavior in different ways while collecting multiple types of data (audiovisua recordings, speech data, gameplay data, human perceptions). Results showed significant differences between English and Korean speakers during the experiment. Korean speakers spoke less on average and had more negative speech sentiment, while the English speakers spoke more frequently and had more positive speech sentiment. The avatar was also more likely to interrupt the human's speech in English than Korean, despite having the same design. Furthermore, Korean speakers perceived more social presence when the avatar engaged in more repetitive speech behavior, while English speakers perceived more when the avatar was more “chatty”. We suggest that these results likely relate to cultural differences between East Asian cultures and Western cultures in terms of the social norms that govern appropriate social interaction behavior, and discuss the implications for future work on interactive speech agents.

#### 2.3 Keywords
Human-robot interaction; Social cognition; Speech system; Virtual avatar; Language differences; Cross-cultural robotics

## 3. Features
- **Automatic Speech Recognition (ASR)**: Recognizes player's speech and responds based on keyword files.
- **Text-to-Speech (TTS)**: Synthesizes utterances using Microsoft Azure TTS SDK.
- **Game State Parsing**: Reads and processes game states from CSV files, updating the state based on player actions and game events.
- **Decision Tree Parsing**: Uses a decision tree structure to determine appropriate responses based on the game state.

## 4. Versions
The project is available in two versions:
- **Korean**: Contains scripts with Korean annotations and is tailored for Korean gameplay interactions.
- **English**: Contains scripts with English annotations and is tailored for English gameplay interactions.

## 5. Directory Structure
- **2021 Experiment**:
  - **Korean** and **English**: Both versions have the following structure:
    - **Control_condition**: 
      - Planning: OFF
      - Responsiveness: HIGH/MAX (Chattiness = 3)
      - IOR: ON (Repetition Delay / REP_DELAY_AMT = 3)
    - **H2_condition**: 
      - Planning: OFF
      - Responsiveness: LOW (Chattiness = 1.5)
      - IOR: ON (Repetition Delay / REP_DELAY_AMT = 3)
    - **H3_condition**: 
      - Planning: OFF
      - Responsiveness: HIGH/MAX (Chattiness = 3)
      - IOR: OFF (Repetition Delay / REP_DELAY_AMT = 0)
  - **setting**: Contains experiment condition explanations and

## 6. Setup
1. Install dependencies from `requirements.txt`.
2. Set up Microsoft Azure API keys in `config.py`.
3. Run `__main__.py`.

## 7. Note
Ensure removal of API keys and check files for sensitive information before sharing.

## 8. Acknowledgements
This work was supported by a grant from the National Research Foundation of Korea (NRF) (Grant number:2021R1G1A1003801).
