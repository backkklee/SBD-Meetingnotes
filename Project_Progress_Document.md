## Goal
- Pull recent record from Webex -> STT > text -> NLP > meeting report

## Day 1: 29/12/2025
- Done: Draft workflow using n8n, research STT and NLP AI models
STT: OpenAI whisper v3 (turbo reduce accuracy WER 5-10% but increase performance x2) 
https://huggingface.co/openai/whisper-large-v3
https://huggingface.co/openai/whisper-large-v3-turbo
NLP: VietAI vit5 (open source)
https://huggingface.co/VietAI/vit5-large-vietnews-summarization
 - Problem: Find requirements to pull records (calling Webex API), use AI models 
- Next: Find information, requirements about the AI models:
STT: Consider Gemini instead of OpenAI whisper v3
NLP: Consider other documents targeted models 
General requirements for workflow (webhook, deploy, cloud, ...)

## Day 2: 30/12/2025
- Done: Change models to google cloud vertex AI for both STT and NLP -> free tier.
- Problem: Did not call API, set up service account
- Next: Set up service account, call API
## Day 3: 5/1/2025
- Done: Use built in Gemini nodes in n8n instead of requesting HTTP for google cloud vertex AI. Set up credentials and service account to call API.
- Problem: Can not call API, error 403 - permission error
- Next: Fix error or change model
## Day 4: 6/1/2025
- Done: Finish fixing error, error comes from the permission of the input file in google storage is not public. Finish 50% of the workflow.
- Problem: 
- Next: Setting up webhook to call Webex API, convert meeting recording to mp3 files then finish the workflow.