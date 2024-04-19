A chord guesser that I wrote to predict chords in songs, using sklearn's KNN interface.

As of right now, what it can do is it takes in data of singular chords from https://zenodo.org/records/5217057
Each chord has 100 samples. To do training, I take the first 80 of each chord type and train it on them. After training, I do cross validation with the last 20 chords of each chord type. This seems to be working consistently well.

Next, we utilize this to predict chord progressions in songs. This is still a WIP. Some open questions:

1) Songs are dynamic - need to find a good way to identify when chords change
2) Right now the focus is on Triads. How to identify non-triad chords?
3) Sometimes music is weird and weird chords are used. How to identify supporting chords during dissonances?
