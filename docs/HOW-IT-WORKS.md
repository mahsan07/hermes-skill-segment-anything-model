# How Segment Anything Model Works

The visuals on this page are static SVGs, so they render directly on GitHub on phones and desktop browsers. Each one is generated from a model specific to this skill.

## System architecture

![Detailed system map for Segment Anything Model](../assets/system-map.svg)

### Components

- **1. Source image:** participates in load and normalize the source image.
- **2. Point box or mask prompt:** participates in choose positive points boxes or prior mask.
- **3. SAM image encoder:** participates in encode image features once.
- **4. Mask decoder:** participates in decode candidate object masks.
- **5. Segmentation overlays:** participates in compare confidence and edge quality.

## Actor and data sequence

![Actor and data sequence for Segment Anything Model](../assets/operation-sequence.svg)

### 1. Load and normalize the source image

**Primary surface:** `Source image`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 2. Choose positive points boxes or prior mask

**Primary surface:** `Point box or mask prompt`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 3. Encode image features once

**Primary surface:** `SAM image encoder`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 4. Decode candidate object masks

**Primary surface:** `Mask decoder`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 5. Compare confidence and edge quality

**Primary surface:** `Segmentation overlays`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.
### 6. Export mask cutout and overlay preview

**Primary surface:** `Source image`

Record the concrete input, the operation performed, and the evidence produced at this stage. Continue only when the output is sufficient for the next stage; otherwise preserve the blocker and stop.

## Example output shape

![Illustrative output for Segment Anything Model](../assets/example-output.svg)

The example is a visual contract: a real run may look different, but it should expose comparable state, provenance, and verification information. It is not presented as evidence of a live external action.

## Decision and stop conditions

![Decision guide for Segment Anything Model](../assets/decision-guide.svg)

The workflow stops when the target is ambiguous, the relevant surface is unavailable or unauthorized, or the final artifact cannot be checked. A logged-in session or successful tool call is not by itself proof that the requested outcome is complete.

## Verification checklist

- Confirm every component shown in the system map exists in the target environment.
- Trace the actor sequence using actual tool output or artifact state.
- Compare the result with the example-output information contract.
- Re-read or reopen the final artifact instead of trusting an attempt message.
- Report omitted stages, unsupported capabilities, and remaining human decisions.
