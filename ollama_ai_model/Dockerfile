# use the official ollama image (CPU will be used when no GPU is present)
FROM ollama/ollama:latest

# Optional: pull at build time so model is present (can increase build time)
# RUN ollama pull llama3

EXPOSE 11434

CMD ["serve"]
