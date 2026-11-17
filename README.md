# MiniMax H3

Generate MiniMax H3 video and H3 Image with the Phosor API.
Video accepts text, a start image, or references, and includes native audio.
H3 Image takes one prompt, any aspect ratio, up to 4K.

768p video is $0.012 per second. H3 Image is $0.0175 at 1K and $0.055 at 4K.
The price shown when you submit is the price you pay.

## Text to video

```bash
curl https://phosor.ai/api/v1/inference/submit \
  -H "X-API-Key: $PHOSOR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "minimax/h3/text-to-video",
    "prompt": "A person walks across a quiet street at dusk.",
    "duration": 5,
    "resolution_tier": "768p",
    "aspect_ratio": "16:9"
  }'
```

Image to video uses `minimax/h3/image-to-video`.
Reference to video uses `minimax/h3/reference-to-video`.

Phosor: https://phosor.ai/?utm_source=github&utm_medium=referral&utm_campaign=h3_lowest_price_202611&utm_content=github_en_03

H3 Image: https://phosor.ai/models/minimax-h3-image
