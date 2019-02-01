# pseudolocalize

A simple webpage to pseudo-localize your texts.
Super useful if you cater to non-English users as well and do not wish to test your UI layouts across different languages.

This is inspired from: [Pseudo Localization @ Netflix](https://medium.com/netflix-techblog/pseudo-localization-netflix-12fff76fbcbe)

**The problem that Netflix aimed to solve was:**

Expansion of text due to translation causes most of the UI layout issues we detect during localization testing.
When translating into other languages, the translated text could be up to 40% longer than the English. This is more prevalent in German, Hebrew, Polish, Finnish, and Portuguese.

**Their solution was:**

Enter Pseudo Localization. Pseudo Localization is a way to simulate translation of English UI strings, without waiting for, or going to the effort of doing real translation. Think of it as a fake translation that remains readable to an English speaking developer, and allows them to test for translation related expansion, among other important things.

In my implementation of pseudo localization, I'd be using this algorithm:

- Multiplying the vowels to increase the length without losing readability
- Transformation of ASCII characters to extended character equivalents
