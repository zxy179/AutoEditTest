# AutoEditTest

AutoEditTest is a coverage-guided semantic fuzzing framework for testing
text-based image editing models.

## Overview

Text-based image editing models generate edited images according to natural
language instructions. However, their open-ended outputs make it difficult to
automatically generate valid test cases, explore diverse semantic behaviors,
and identify editing failures without ground-truth reference images.

AutoEditTest addresses these challenges through three main components:

1. **Target-Grounded Test Generation**  
   Constructs image-editing instructions from the visual content of the target
   region and its surrounding scene context, improving the semantic consistency,
   executability, and checkability of generated test cases.

2. **Coverage-Guided Semantic Fuzzing**  
   Represents editing requirements using atomic semantic buckets, including
   object, color, count, material, shape, size, and spatial relation. Coverage
   feedback guides subsequent generation toward under-explored semantic values.

3. **Ground-Truth-Free Test Oracle**  
   Uses a dual-branch oracle to detect editing failures. The non-target branch
   checks whether unrelated image regions are preserved, while the target-side
   branch converts editing requirements into structured Yes/No visual questions
   to verify whether the requested edit has been correctly performed.

## Framework

The AutoEditTest workflow contains four stages:

1. Target-grounded context construction
2. Executable-and-checkable instruction synthesis
3. Atomic-bucket coverage feedback
4. Dual-branch ground-truth-free oracle

## Repository Status

This repository currently provides an introduction to the AutoEditTest project.
The source code and detailed documentation will be released later.

## Contact

For questions about this project, please open an issue in this repository.
