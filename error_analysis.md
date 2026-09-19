# Error Analysis

The model was reviewed on weak predictions from the test images.

| Case | Image | Error Type | Possible Reason |
|---:|---|---|---|
| 1 | hard_hat_workers1022.png | Person missed | Crowded scene and occlusion |
| 2 | hard_hat_workers1351.png | Helmet missed | Low-light image |
| 3 | hard_hat_workers2409.png | Loose person box | Complex background |
| 4 | hard_hat_workers2517.png | Overlapping boxes | Many nearby workers |
| 5 | hard_hat_workers3087.png | Helmet missed | Small object size |
| 6 | hard_hat_workers3241.png | Head missed | Very few head examples |
| 7 | hard_hat_workers3862.png | Low confidence | Occlusion and image scale |
| 8 | hard_hat_workers4075.png | Poor localization | Similar visual pattern |
| 9 | hard_hat_workers4851.png | Person missed | Difficult viewpoint |
| 10 | hard_hat_workers857.png | Overlapping predictions | Crowded workplace scene |

The helmet class performed best. The head class performed poorly because it was underrepresented. Improvements include collecting more balanced data, improving annotations, adding low-light and crowded examples, and training for more epochs.
