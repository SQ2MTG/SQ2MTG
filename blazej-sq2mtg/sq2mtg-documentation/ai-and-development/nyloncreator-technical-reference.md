# NylonCreator — technical reference

## Purpose

NylonCreator is a project for applying hosiery patterns to uploaded images through a Python/OpenCV backend and a web frontend.

## Processing pipeline

Previously documented source inspection identifies this flow:

`image + pattern upload → polygon mask → /apply-patterns/ → OpenCV fill/resize/masked replacement → generated result`.

An `/auto-segment/` endpoint uses a SAM ViT-B model and selects a large contour for segmentation.

## Backend

The project uses FastAPI/Uvicorn, Python, OpenCV, NumPy, multipart upload handling and PyTorch/torchvision. SAM weights are supplied separately.

Documented endpoints include upload, pattern application, automatic segmentation and result retrieval.

## Storage

The documented working directories are:

* `uploads/`
* `patterns/`
* `results/`

## Security

The current implementation documentation identifies permissive CORS configuration. Production deployments should narrow allowed origins and review credentialed CORS settings.

Uploaded files require strict size, MIME/content validation and safe filename handling. Result and source directories should not be exposed as unrestricted public file stores.

## Hardware

SAM inference can use CUDA or CPU. Exact VRAM requirements depend on model/runtime configuration.
