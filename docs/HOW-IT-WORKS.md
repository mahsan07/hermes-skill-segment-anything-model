# How Segment Anything Model Works

Use SAM for zero-shot image segmentation with points, boxes, or masks.

![Detailed systems blueprint for Segment Anything Model](../assets/system-blueprint.png)

## Stages

### 1. Load and normalize the source image

**Primary surface:** `Source image`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 2. Choose positive points boxes or prior mask

**Primary surface:** `Point box or mask prompt`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 3. Encode image features once

**Primary surface:** `SAM image encoder`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 4. Decode candidate object masks

**Primary surface:** `Mask decoder`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 5. Compare confidence and edge quality

**Primary surface:** `Segmentation overlays`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.
### 6. Export mask cutout and overlay preview

**Primary surface:** `Segmentation overlays`

Record the input, operation, observable output, and any decision that changes scope. Stop here if the output is missing, contradictory, or insufficient for the next stage.

## Failure handling

- **Authorization failure:** do not probe credentials or broaden access; report the missing authority.
- **Target ambiguity:** stop before mutation and request the minimum identifying information.
- **Tool or service failure:** retain error evidence, retry only safe transient failures, and cap retries.
- **Verification failure:** classify the run as incomplete even when the preceding operation returned success.

## Completion evidence

The handoff should contain the original request, inspection state, preview or plan, exact execution result, direct verification, and a final receipt naming limitations and withheld actions.
