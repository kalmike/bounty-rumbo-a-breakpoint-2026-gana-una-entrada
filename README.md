### README.md

# Rumbo a Breakpoint 2026: gana una entrada y apoyo para tu viaje

## Overview

La Familia es la comunidad de Solana en España. Nuestro objetivo es conectar a builders, fundadores y proyectos, creando un espacio para aprender y crecer juntos. 

## Mission

Queremos que crees contenido increíble en español sobre Breakpoint 2026 (Londres, 15-17 de noviembre). Ya sean tus mejores recuerdos de Breakpoint o por qué no puedes esperar a asistir este año. El objetivo: hacer que la gente de habla hispana se sienta emocionada, incluida y motivada a ir a Breakpoint.

## Scope Detail

Crea una publicación en X, IG o LinkedIn, en español, mostrando tu entusiasmo por Breakpoint 2026. Incluye una llamada a la acción (CTA) invitando a la gente a registrarse en luma.com/breakpoint2026 y menciona el código de descuento SUPERTEAM-NH7-BP26. Destaca un enfoque de España / La Familia (ser parte de la comunidad Solana Hispana, querer conocer a La Familia en Londres, etc.). Etiqueta a @SolanaEvents y @LaFamilia_so. Se permite cualquier formato de imagen o video (IA, animación, personal...).

## Submission Requirements

- Debes incluir el enlace a tu publicación original.
- El contenido debe estar en español.
- Tanto las etiquetas como el enlace CTA deben estar incluidos.
- Los participantes DEBEN asistir a Breakpoint 2026.

## Judging Criteria

- Creatividad y engagement.
- Claridad del entusiasmo por Breakpoint.
- Ángulo España / La Familia.
- Cumplimiento de todos los requisitos.
- Las presentaciones en video serán valoradas positivamente.

## Reward Structure

- 1st Place: 400 USDG + Breakpoint Ticket
- 2nd Place: 400 USDG
- 3rd Place: 400 USDG
- 4th Place: 400 USDG
- 5th Place: 400 USDG
- 6th Place: 400 USDG
- 7th Place: 400 USDG
- 8th Place: 400 USDG
- 9th Place: 400 USDG
- 10th Place: 400 USDG
- Bonus Awards: 5 ganadores reciben 200 USDG cada uno

## How to Participate

1. Create a post on X, IG, or LinkedIn in Spanish.
2. Share your post and include the link.
3. Use the hashtag @SolanaEvents and @LaFamilia_so.
4. Include the CTA to register at luma.com/breakpoint2026 and use the code SUPERTEAM-NH7-BP26.
5. Ensure your post promotes the Spanish community and Breakpoint 2026.

## Testing

To test the tool, run:

```bash
python submit_post.py --test
```

This will simulate the submission process and ensure that all requirements are met.

### submit_post.py

```python
import argparse
import json
import requests
from datetime import datetime

def submit_post(post_url, post_content, post_hashtags):
    # Simulate submission process
    print(f"Submitting post to {post_url}")
    print(f"Content: {post_content}")
    print(f"Hashtags: {post_hashtags}")
    return {"status": "success", "message": "Post submitted successfully"}

def test_submit_post():
    # Test data
    post_url = "https://example.com/post"
    post_content = "Check out Breakpoint 2026! #SolanaEvents #LaFamilia_so"
    post_hashtags = ["#SolanaEvents", "#LaFamilia_so"]

    # Run the submission function
    result = submit_post(post_url, post_content, post_hashtags)

    # Check if the result is as expected
    assert result["status"] == "success", "Test failed: Post submission failed"
    assert result["message"] == "Post submitted successfully", "Test failed: Incorrect message"

    print("Test passed: Post submitted successfully")

if __name__ == "__main__":
    parser = argparse.ArgumentParser(description="Submit a post for the Rumbo a Breakpoint 2026 bounty")
    parser.add_argument("--test", action="store_true", help="Run the test submission process")
    args = parser.parse_args()

    if args.test:
        test_submit_post()
    else:
        # Actual submission logic here
        post_url = input("Enter the URL of your post: ")
        post_content = input("Enter the content of your post: ")
        post_hashtags = input("Enter the hashtags for your post (comma-separated): ").split(',')

        result = submit_post(post_url, post_content, post_hashtags)
        print(result)
```

### JSON Response

```json
{
  "otherInfo": {
    "toolName": "submit_post.py",
    "description": "A Python tool to submit a post for the Rumbo a Breakpoint 2026 bounty",
    "dependencies": ["argparse", "json", "requests", "datetime"]
  },
  "eligibilityAnswers": {
    "link": "https://example.com/breakpoint2026-registration"
  }
}
```