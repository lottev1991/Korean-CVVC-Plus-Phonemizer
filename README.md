(This readme is English-only for now, my apologies.)

# Korean CVVC+ Phonemizer
A custom Korean phonemizer for OpenUtau.

This phonemizer was heavily built upon NANA's Korean CVC Phonemizer, which comes with OpenUtau by default.
## Download OpenUtau
If you haven't downloaded OpenUtau yet, you can do so [here](https://github.com/stakira/openutau).
## How to install
### Method #1
- Click on Tags above or on the right in order to get the .dll file.
- Once downloaded, drag and drop ``KoreanCVVCPlusPhonemizer.dll`` onto the OpenUtau program.
### Method #2
- As above, click on Tags.
- When downloaded, move ``KoreanCVVCPlusPhonemizer.dll`` into the ``path\to\OpenUtau\Plugins`` folder.
### What is "Korean CVVC+"?
It's a name for my own method of Korean in UTAU. It's heavily based upon Syeon's Korean CVVC list, which is unfortunately no longer online. I've adjusted it to be a bit more expansive. I will release the reclist and an accompanying voicebank sometime in the future.
#### How syllables work
Syllables are built like this:
- Starting CV: ``[- cv]`` (optional);
- VV (includes VCV with 의 (eui)): ``[v v]`` (optional);
- Connecting CV: ``[cv]`` **(required)**;
- Connecting VC: ``[v c]`` (optional);
- Batchim (syllable finals): ``[v C]`` **(required)**;
- Connecting CC (to connect notes ending in batchim): ``[C c]`` (optional);
- Vowel/sonorant batchim (N, L, M, NG) endings: ``[v R]``/``[C R]`` (optional);
- Vowel/sonorant batchim (N, L, M, NG) end breaths: ``[v H]``/``[C H]`` (optional);
- Vowel/sonorant batchim (N, L, M, NG) end inhales: ``[v B]``/``[C B]`` (optional);
- Glottal stops for vowels and sonorant batchim: ``[・ v]``/``[・ C]``(CV) + ``[v ・]``/``[C ・]``(VC) (optional).
#### Other notes on syllables
- This phonemizer merges ㅐ(ae) and ㅔ(e).
- This phonemizer supports sandhi/liaison and allophones (i.e. sound changing processes depending on context), although it does have some known bugs (which are mostly a leftover from the Korean CVC Phonemizer). I might try to fix those in the future.
- When a connecting CV note contains:
  - a semivowel (so, any vowel starting with "y" or "w"),
  - the vowel ㅣ(i),
  - the vowel ㅗ(o) or ㅜ(u),

  the VC will treat the consonant as either rounded or palatalized (depending on the vowel), e.g. ``[v cy]``/``[v cw]``
- The main difference between connecting VC and batchim, is that batchim uses capital letters for the consonants, whereas connecting VC uses lowercase.
- This phonemizer supports some Konglish sounds (i.e. "Engrish" with a Korean voicebank):
  - "f";
  - "v";
  - "z";
  - "th";
  - "rr" (English "r" starting sound);
  - "er" (English "r" rhotic vowel).
- As you can see above, the phonemizer only needs basic CV and batchim notes, the rest is optional. So in theory, you could create a "CV + batchim" bank (with capital letters!) and it would be fully functional with this phonemizer.
### !! Non-Korean users on Windows: PLEASE READ !!
While this phonemizer does support rudimentary romaja input (i.e. no automatic batchim is applied), it is highly recommended to use Hangul unless you're doing Konglish. For Mac users, this is not a problem since a romaja-based QWERTY Korean keyboard comes with OSx by default. However, for Windows, by default, there is not. This is very impractical for users who either can't read Hangul and/or who do not own keyboard stickers.

Thankfully, there is a solution for this: Nalgaeset, a Korean keyboard software for Windows, which you can download [here](http://moogi.new21.org/en/ngs/index.htm).

Nalgaeset has many options, including a popular setting for romaja-based QWERTY Hangul input. So, if you type "ga" with the Hangul QWERTY keyboard setting, it will correctly convert to 가.

A more detailed explanation of how it works is explained on the download page linked above. I recommend that you give it a read before using it.

This software is of course also of course very handy for using OpenUtau's in-built Korean phonemizers.
### Got any issues?
Feel free to leave those on the Issues tab! I'll make sure to take a look.

Please note that I sadly do not know Korean, so I can only respond to issues in English. However, you don't need to know English in order to submit an issue, we thankfully have machine translation for that.
### Have a function to add?
Feel free to make a pull request! You can also leave ideas in the Issues tab, although I can't guarantee I'm able to implement everything. Of course, maybe someone else might pick up your idea for their own PR.
### Will I ever submit this phonemizer upstream?
Only if there's enough demand for it. There are already so many in-built Korean phonemizers and I'd rather not make it too excessive. That's why I've decided to make it a separate plugin for now instead.
### I'd like to translate this readme to Korean!
Yes please! Help with that would be much appreciated.
