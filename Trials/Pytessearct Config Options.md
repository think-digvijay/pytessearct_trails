# Pytessearct Config Options

1. PSM: Page segmentation mode
    0    Orientation and script detection (OSD) only.
    1    Automatic page segmentation with OSD.
    2    Automatic page segmentation, but no OSD, or OCR.
    3    Fully automatic page segmentation, but no OSD. (Default)
    4    Assume a single column of text of variable sizes.
    5    Assume a single uniform block of vertically aligned text.
    6    Assume a single uniform block of text. 
    7    Treat the image as a single text line.
    8    Treat the image as a single word.
    9    Treat the image as a single word in a circle.
    10    Treat the image as a single character.
    11    Sparse text. Find as much text as possible in no particular order.
    12    Sparse text with OSD.
    13    Raw line. Treat the image as a single text line,

# Bad Output: 0, 2, 5, 6, 7, 8, 9, 10, 13
# Good Ouptut: 1, 3, 4, 11 & 12(not original structure)

2. OEM: OCR Engine Mode - Which algorithm to use
    **0 = Original Tesseract only.
    **1 = Neural nets LSTM only.
    2 = Tesseract + LSTM.
    **3 = Default, based on what is available.

--------------
Engine Configs:

1. textord_fast_pitch_test:	T
    Do even faster pitch algorithm
    # Try T and F both

2. tessedit_zero_rejection: T
    Dont reject ANYTHING

3. tessedit_minimal_rejection: F
4. tessedit_write_rep_codes: F
5. edges_children_fix: F

6. edges_childarea: 0.65
    Min area fraction of child outline
    # Try 0.5 and values between 0.4-0.6

7. edges_boxarea: 0.9
    Min area fraction of grandchild for box
    # Try values between 0.8-0.9

8. tessedit_train_line_recognizer: T

9. textord_no_rejects: T
    Don’t remove noise blobs
    # Keep True if default is F

10. tessedit_init_config_only: T
