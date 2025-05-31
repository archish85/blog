---
layout: post
title: "Asked ChatGPT to guess the song from my violin recording"
date: 2025-05-31
---

# How ChatGPT helped me record my violin

For long I have dreamt of being able to record my violin directly into a computer and get it to synthesize the audio while recording and being able to monitor it while playing. I have not been very successful at it. Thankfully, now I have an AI agent which patiently helps me with each step. After purchasing an Audio Interface and some TRS cables and a pair of monitors, I was finally able to assemble a modest studio arrangement in my home. It was still not easy, things would never work the way the agent would describe so it took me few days and finally, I managed to get a recording of my violin into my macbook using Garageband.


Here's the recording of my violin:

<audio controls preload="metadata" style="width: 100%;">
  <source src="{{ '/assets/audio/Old Hindi film song - 29:05:25, 7.33 PM.mp3' | relative_url }}" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

# Can you guess the song?

If you're familiar with Old Hindi movie songs, I believe it wouldn't be tough for you to guess it. ChatGPT, however, failed to do so. 

# An insight into how an LLM tries to identify a song

Before this experiment, I had uploaded a hindi song with my flute and using my iphone as a mic, I had naively named the file as the song title 'Husnwaale tera jawab nahi flute.mp3' and uploaded it to ChatGPT and asked it for feedback. The song is composed by Ravi and sang by Mohd Rafi and these became the contextual clues for the model to guess this song, which I had deliberately named 'Old Hindi film song'. The model guessed incorrectly and after 4 clues, was finally able to guess the song.

Curious, I asked it to explain how it tried to guess the song and what it replied was quite insightful:

>Absolutely, Archish — I’ll be fully transparent and walk you through the exact process (spoiler: *yes*, your clues did most of the heavy lifting this time 😅):
>
>---
>
>### 🎧 Step-by-step Breakdown of My (Wobbly) Musical Detective Work:
>
>---
>
>### 1. **Initial Audio Analysis**:
>
>When you uploaded your violin track, I ran it through internal pattern recognition:
>
>* I parsed the **melodic contour** (rise/fall of notes)
>* Listened for **signature phrases or motifs** that typically define old Hindi melodies
>* Looked at **tempo, scale (raag hints), and emotional texture**
>
>But here’s the thing:
>Violin, especially when played solo and without clear rhythmic structure or supporting harmony, can be **tricky to identify** — especially when there are slight variations from the original (because: artistic expression, improvisation, tone difference, or being out of practice as you mentioned). So even if the melody was recognizable, it may not have mapped *cleanly* to a specific song in my database.
>
>So while I *tried* to match it based on melody alone, there wasn't a confident match.
>
>---
>
>### 2. **My First Wild Guess**:
>
>I saw "old Hindi film song" and your previous “Husnwale” performance, and I *thought* I detected similar phrasing — which is why I >guessed “Chaudhvin Ka Chand.”
>That was a complete misfire. No shame in being human–adjacent.
>
>---
>
>### 3. **You Dropped Clue #1 – Lata Mangeshkar**:>
>
>This changed the frame completely. Now I was looking for:
>
>* Female vocals originally
>* A different emotional range — more delicate, romantic, or melancholy
>* Lata-style phrasing — gliding legatos, ornamented meends
>
>So I guessed **“Ajeeb Dastan Hai Yeh”** — a classic Lata melody with a floaty violin-friendly contour. Also wrong.
>
>---
>
>### 4. **Clue #2 – Madan Mohan**:
>
>Now we’re talking precision targeting. Madan Mohan means:
>
>* Ghazal-influenced melodies
>* Rich orchestration
>* Slow, emotionally charged phrasing
>* Lata Mangeshkar as muse for many timeless songs
>
>I ran through known **Madan-Lata** combos that violinists *love* to cover. I guessed “Lag Ja Gale” because it’s the poster child >for haunting beauty on the violin.
>
>Still wrong. 😬
>
>---
>
>### 5. **Clue #3 – Mala Sinha & Dharmendra**:
>
>That was the *sniper scope*. Once you narrowed it to these actors, I checked the crossover between:
>
>* Films starring them together
>* Songs composed by Madan Mohan
>* Sung by Lata
>* With violin-adaptable melodic lines
>
>And **“Aap Ki Nazron Ne Samjha”** from *Anpadh* checks *every single box*:
>
>* Lata ✅
>* Madan Mohan ✅
>* Mala Sinha & Dharmendra ✅
>* Signature violin melody ✅
>* Expressive, emotional and slow enough to be played beautifully on a violin ✅
>
>Bingo. Got it. **But not by ear alone**.
>
>---
>
>### ✅ So, to confirm:
>
>* **Your clues guided me** more than the raw audio.
>* The tune *sounded familiar*, but wasn’t distinct enough to guess confidently without hints.
>* Had you given **no clues**, I would have struggled to pinpoint it *exactly* — unless the violin playing was closer to the film >melody in structure and tempo.
>
>---
>
>And honestly? That’s *not* a reflection on your playing being “bad” at all. It just shows that:
>
>* You're adding your own expression.
>* The piece may not have been note-for-note yet — which is fine.
>* A solo violin lacks lyrics and instrumentation that usually give away the song instantly.
>
>---

My next idea is to perform song with backing tracks and see if I can get better response from the model. I am still learning the ropes of garageband and audio recording and it's an exciting journey and I want to see how the model develops as I keep developing my skills.

