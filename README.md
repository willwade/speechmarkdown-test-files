## Speech Markdown Test Files

The open source version of the Speech Markdown Test Files

The files contained in this project are to assist those writing parsers, formatters, libraries, and other software to have a consistent set of test data files.

These files are not for a specific testing framework, rather they contain Speech Markdown formatted text and what the corresponding text would be after a formatter has converted it. Samples are shown for Plain Text as well as platform-specific Speech Synthesis Markup Language (SSML).

Each group of test files are in their own folder and file naming follows this convention:

| extension             | description                      |
| --------------------- | -------------------------------- |
| `.smd`                | Speech Markdown input            |
| `.txt`                | Converted to Plain Text          |
| `.alexa.ssml`         | SSML - Amazon Alexa              |
| `.polly.ssml`         | SSML - Amazon Polly              |
| `.polly-neural.ssml`  | SSML - Amazon Polly Neural       |
| `.google.ssml`        | SSML - Google Assistant          |
| `.azure.ssml`         | SSML - Microsoft Azure           |
| `.sapi.ssml`          | SSML - Microsoft SAPI            |
| `.w3c.ssml`           | SSML - W3C                       |
| `.samsung.ssml`       | SSML - Samsung Bixby             |
| `.apple.ssml`         | SSML - Apple AVSpeechSynthesizer |
| `.watson.ssml`        | SSML - IBM Watson                |
| `.elevenlabs.ssml`    | SSML - ElevenLabs                |
| `.acapela-cloud.ssml` | SSML - Acapela Cloud             |
| `.acapela.ssml`       | Native tags - Acapela Desktop    |

All data files are under the `test-data` folder.

### Platform-specific tests

Some test cases only generate output for the relevant platform(s). For example, `azure-style-*` tests only produce `.azure.ssml` output since Azure-specific features (like emotional styles) have no equivalent on other platforms.

### Test case categories

| category         | examples                                                                                                                                                                                                                      |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Breaks           | `break-short`, `break-time`, `break-strength`                                                                                                                                                                                 |
| Emphasis         | `emphasis-standard-*`, `emphasis-short-*`                                                                                                                                                                                     |
| Say-as           | `address-standard`, `number-standard`, `characters-standard`, `date-standard`, `time-standard`, `telephone-standard`, `ordinal-standard`, `fraction-standard`, `expletive-standard`, `interjection-standard`, `unit-standard` |
| Prosody          | `rate-standard-*`, `pitch-standard-*`, `volume-standard-*`, `prosody-multiple-modifiers *`                                                                                                                                    |
| Phonemes         | `ipa-standard`, `ipa-standard-alphabet-*`, `ipa-short`, `bare-ipa`                                                                                                                                                            |
| Substitution     | `sub-standard`, `sub-short`                                                                                                                                                                                                   |
| Modifiers        | `whisper-standard`, `lang-standard`, `timbre-standard`, `drc-standard`, `multiple-modifiers-same-text`                                                                                                                        |
| Voice & Sections | `voice-standard*`, `sections-standard*`, `dj-section*`, `newscaster-section*`                                                                                                                                                 |
| Expressive tags  | `expressive-laugh`, `expressive-cough`, `expressive-sigh`, `expressive-multiple`, etc.                                                                                                                                        |
| Azure styles     | `azure-style-cheerful`, `azure-style-sad`, `azure-style-angry`, `azure-section-*`, `azure-role-*` (Azure only)                                                                                                                |
| Audio            | `audio-standard`, `audio-with-caption`                                                                                                                                                                                        |
| Mark             | `mark-standard`                                                                                                                                                                                                               |
| Edge cases       | `escape-xml-characters`, `say-as-modifiers last modifier wins`, `modifier-text-allowed-chars *`                                                                                                                               |

### Regenerating fixtures

Fixtures are generated from the [speechmarkdown-js](https://github.com/speechmarkdown/speechmarkdown-js) reference implementation using `scripts/generate-test-fixtures.ts`. The script preserves existing files and only adds missing platform outputs.

We welcome your contributions to improving this project. All submissions will be reviewed for technical accuracy and possibly reworded to comply with style guidelines required by our editorial team.

The goal of this project is to support voice designers, developers, and tool creators in adoption and enhancement of Speech Markdown. We want you to be successful. If this project is not helping you achieve your goals, then please let us know where we can do a better job. Thank you for your contributions!

## License Summary

The documentation is made available under the Creative Commons Attribution-ShareAlike 4.0 International License. See the LICENSE file.

The sample code within this documentation is made available under a modified MIT license. See the LICENSE-SAMPLECODE file.
