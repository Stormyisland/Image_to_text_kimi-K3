# Image_to_text_kimi-K3

What It Does
Creates an InferenceClient using HF_TOKEN.

Sends a chat completion request to moonshotai/Kimi-K3.1-Pro:together with a text prompt and an image URL.

Prints completion.choices[0].message — the model's one-sentence description.

Customize
Prompt → content[0].text

Image → content[1].image_url.url (public URL or data:image/jpeg;base64,...)

Model → model= argument

Troubleshooting
Error	Fix
KeyError: 'HF_TOKEN'	Export the env var before running
401 Unauthorized	Token invalid or missing Inference permissions
404 model not found	Check the model ID and :together suffix
429 rate limit	Free-tier quota exceeded — wait or upgrade
Notes
Image URL must be publicly accessible.

The :together suffix routes to the Together provider (needed for vision support).

Requests consume your HF Inference credits.


