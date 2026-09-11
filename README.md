# AutoEditTest

<p align="center">
  <b>English</b> | <a href="./README_CN.md">简体中文</a>
</p>

## Overview

**AutoEditTest** is a coverage-guided semantic fuzzing framework for testing
text-based image editing models.

Text-based image editing models generate edited images according to natural
language instructions. However, their open-ended outputs make it difficult to
generate valid test cases, explore diverse semantic behaviors, and identify
editing failures without ground-truth reference images.

## Method

AutoEditTest consists of four main stages:

### 1. Target-Grounded Context Construction

AutoEditTest detects and segments the target object, then combines its category,
visual description, and scene context to construct target-grounded multimodal
information.

### 2. Executable-and-Checkable Instruction Synthesis

Based on the target context and editing-task taxonomy, AutoEditTest generates
natural-language editing instructions together with structured attribute records,
ensuring that test inputs are semantically consistent, executable, and checkable.

### 3. Atomic-Bucket Coverage Feedback

AutoEditTest decomposes editing requirements into atomic semantic buckets, such
as object, color, count, material, shape, size, and spatial relation. Coverage
feedback guides subsequent generation toward under-explored semantic values.

### 4. Dual-Branch Ground-Truth-Free Oracle

AutoEditTest detects editing failures through:

- **Non-target preservation:** checks whether unrelated image regions are
  unintentionally modified.
- **Target-side alignment:** converts editing requirements into structured
  Yes/No visual questions and verifies whether the requested edit is satisfied.

## Repository Status

This repository currently provides an introduction to AutoEditTest. Source code,
experimental data, and detailed documentation will be released later.

## Contact

For questions about this project, please open an issue in this repository.
