# TMPD: 10-Sample Preview

This directory contains a small, non-exhaustive preview of TMPD for inspecting
the data schema. It is not an official train/validation/test split and must not
be used to report benchmark performance.

## Contents

- `samples.csv`: tabular metadata and 30 daily popularity targets.
- `samples.jsonl`: the same records with the trajectory stored as a list.
- `images/`: one image for each sample, renamed to match `sample_id`.
- `SHA256SUMS`: checksums for integrity verification.

## Fields

| Field | Description |
|---|---|
| `sample_id` | Demo-only identifier; original platform IDs are excluded. |
| `image_path` | Relative path to the local image. |
| `publication_time` | Topic publication timestamp. |
| `title`, `content` | Topic title and associated textual content. |
| `category` | English category label. |
| `publisher_name` | Public publisher display name. |
| `publisher_location` | Public profile location. |
| `publisher_followers`, `publisher_posts` | Public publisher statistics. |
| `topic_length`, `content_length` | Structured length attributes. |
| `popularity_day_01` ... `popularity_day_30` | Preprocessed 30-day popularity trajectory used by the released experiments. |

## Privacy and data notice

Direct platform user IDs, post IDs, source topic IDs, and original image URLs
have been excluded. Images are re-encoded to remove embedded metadata. Text and
images may remain subject to the rights and terms of their original platforms
or creators. Inclusion in this academic preview does not grant a separate
license to third-party content. Verify redistribution permissions before making
the repository public and provide a takedown contact in the repository.
