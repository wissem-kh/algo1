# algo1
function analyzeSentence(sentence) {
    let sentenceLength = 0;
    let wordCount = 0;
    let vowelCount = 0;
    const vowels = "aeiouAEIOU";

    for (let i = 0; i < sentence.length; i++) {
        let char = sentence[i];
        sentenceLength++;

        if (char === " " || i === sentence.length - 2) {
            wordCount++;
        }

        if (vowels.includes(char)) {
            vowelCount++;
        }
    }

    if (sentence[sentence.length - 1] === ".") {
        wordCount++;
    }

    return { sentenceLength, wordCount, vowelCount };
}

let sentence = "This is a sample sentence.";
let result = analyzeSentence(sentence);
console.log("Sentence length:", result.sentenceLength);
console.log("Word count:", result.wordCount);
console.log("Vowel count:", result.vowelCount);
