ALGORITHM AnalyzeSentence
  // --- Initialization ---
  length ← 0          // counts every character
  words  ← 1          // start at 1 word; each space marks a new word
  vowels ← 0          // counts a, e, i, o, u (case‐insensitive)

  REPEAT
    READ ch           // read next character from input
    length ← length + 1

    IF ch = ' ' THEN
      words ← words + 1
    END_IF

    IF ch ∈ { 'a','e','i','o','u',
               'A','E','I','O','U' } THEN
      vowels ← vowels + 1
    END_IF

  UNTIL ch = '.'      // stop once the period is read

  // --- Output results ---
  PRINT "Length: ", length
  PRINT "Words:  ", words
  PRINT "Vowels: ", vowels
END_ALGORITHM
