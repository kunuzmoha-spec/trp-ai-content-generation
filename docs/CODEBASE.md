# Codebase Overview

This project is a multi-provider AI content generation framework designed to generate music, video, and images through a unified CLI.

## High-Level Architecture

The system is organized around a modular architecture where providers, pipelines, and presets are separated for extensibility.

The core package lives under `src/ai_content/`.

## Key Directories

- `cli/`  
  Implements the command-line interface using Typer. This is the main entry point for users.

- `providers/`  
  Contains integrations for different AI providers such as Google (Gemini, Veo, Imagen) and Minimax (via AIMLAPI). Each provider follows a common interface.

- `pipelines/`  
  Defines multi-step workflows (e.g., music → video, image → video). Pipelines orchestrate calls between providers.

- `presets/`  
  Contains predefined styles, BPMs, moods, and aspect ratios used to standardize generation outputs.

- `core/`  
  Shared orchestration logic used across commands and pipelines.

- `integrations/`  
  Handles communication with external APIs and services.

- `utils/`  
  Helper utilities used across the project.

## Examples

The `examples/` directory demonstrates basic usage:
- Music generation
- Video generation
- Lyrics-based workflows
- Image-to-video pipelines

These examples serve as reference implementations for the CLI commands.

---

## Reference Exploration Notes

The `trp1-ai-artist` repository was explored as the reference implementation for this challenge.

Observations from exploration:
- The project is implemented as a CLI-first framework.
- Providers, pipelines, and presets are cleanly separated.
- The `examples/` directory demonstrates end-to-end workflows for music and video generation.
- The architecture favors extensibility over tightly coupled logic.

No changes were made to the reference repository.
