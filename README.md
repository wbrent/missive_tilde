# missive_tilde

[missive~] is a vector synth object that uses a wavetable index to crossfade between neighboring wavetables in a set. Sets can contain any number of wavetables, and are composed of individual .wav files that each contain one wavetable cycle. The lengths of wavetables in a set need not match. Smooth wraparound is handled automatically (the extra guard points required for Pd's 4-point interpolation scheme are added internally).

The creation argument to [missive~] is the full path to a wavetable set (i.e., a directory containing wavetable cycle .wav files). This can be changed on the fly by passing in a full path via the "set" message. Note that the order of wavetable loading is determined by the .wav file names themselves as they are listed by Pd's [file glob] object. The easiest way to control ordering is to prepend numbers to the .wav file names in your set directory (e.g., 0-hiss.wav, 1-hum.wav, 2-buzz.wav, etc.).
