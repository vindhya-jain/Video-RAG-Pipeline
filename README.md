# Video-RAG-Pipeline

### High-Level Workflow of the Pipeline
* Video Download: Download educational videos from YouTube using yt-dlp.
* Metadata Extraction: Extract metadata (title, description, duration, resolution, etc.) from each video.
* Transcript Extraction: Use Whisper ASR to transcribe the video’s audio, which was in Hindi, and then translate it to English. 
* Keyframe Extraction and Description Generation: Extract keyframes from the video at 5-second intervals and generate captions for each keyframe using the BLIP model.
* Data Embedding and Storage: Embed the transcript text and keyframe descriptions using SentenceTransformer, and store them in ChromaDB for efficient retrieval.
* Query and Search: Based on a query, search for relevant video segments (transcripts or keyframes). The query is converted into a vector and compared against the stored embeddings.
* Results Display: Display the top search results and visualize relevant keyframes or transcripts from the video.
