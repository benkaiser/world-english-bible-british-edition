This project is a fork of [TehShrike/world-english-bible](https://github.com/TehShrike/world-english-bible) but with the underlying data switched to the [British Edition](https://ebible.org/engwebpb/) of the World English Bible. Everything else remains intact.

---

A folder full of JSON files containing a programmatic version of the [World English Bible](http://ebible.org/web/).

Besides the verse text, contains all of the metadata needed to print the text with proper formatting.

Each JSON file contains a flat array of objects.

The file names are all the book names from the [books-of-the-bible](https://github.com/TehShrike/books-of-the-bible) package, lowercased, with spaces removed.

Some examples:

```json
[
/* snip */
	{
		"type": "paragraph start"
	},
	{
		"type": "paragraph text",
		"chapterNumber": 9,
		"verseNumber": 17,
		"sectionNumber": 1,
		"value": "“Now therefore, our God, listen to the prayer of your servant, and to his petitions, and cause your face to shine on your sanctuary that is desolate, for the Lord’s sake.  "
	},
	{
		"type": "paragraph text",
		"chapterNumber": 9,
		"verseNumber": 18,
		"sectionNumber": 1,
		"value": "My God, turn your ear, and hear. Open your eyes, and see our desolations, and the city which is called by your name; for we do not present our petitions before you for our righteousness, but for your great mercies’ sake.  "
	},
	{
		"type": "paragraph text",
		"chapterNumber": 9,
		"verseNumber": 19,
		"sectionNumber": 1,
		"value": "Lord, hear. Lord, forgive. Lord, listen and do. Don’t defer, for your own sake, my God, because your city and your people are called by your name.” "
	},
	{
		"type": "paragraph end"
	},
	{
		"type": "break"
	},
	{
		"type": "paragraph start"
	},
	{
		"type": "paragraph text",
		"chapterNumber": 9,
		"verseNumber": 20,
		"sectionNumber": 1,
		"value": "While I was speaking, and praying, and confessing my sin and the sin of my people Israel, and presenting my supplication before Yahweh my God for the holy mountain of my God;  "
	},
	{
		"type": "paragraph text",
		"chapterNumber": 9,
		"verseNumber": 21,
		"sectionNumber": 1,
		"value": "yes, while I was speaking in prayer, the man Gabriel, whom I had seen in the vision at the beginning, being caused to fly swiftly, touched me about the time of the evening offering.  "
	},
	{
		"type": "paragraph text",
		"chapterNumber": 9,
		"verseNumber": 22,
		"sectionNumber": 1,
		"value": "He instructed me and talked with me, and said, Daniel, “I have now come to give you wisdom and understanding.  "
	},
	{
		"type": "paragraph text",
		"chapterNumber": 9,
		"verseNumber": 23,
		"sectionNumber": 1,
		"value": "At the beginning of your petitions the commandment went out, and I have come to tell you; for you are greatly beloved. Therefore consider the matter, and understand the vision. "
	},
	{
		"type": "paragraph end"
	},
/* snip */
]
```

```json
[
/* snip */
	{
		"type": "paragraph start"
	},
	{
		"type": "paragraph text",
		"chapterNumber": 2,
		"verseNumber": 1,
		"sectionNumber": 1,
		"value": "Hannah prayed, and said: "
	},
	{
		"type": "paragraph end"
	},
	{
		"type": "stanza start"
	},
	{
		"type": "line text",
		"chapterNumber": 2,
		"verseNumber": 1,
		"sectionNumber": 2,
		"value": "“My heart exults in Yahweh! "
	},
	{
		"type": "line break"
	},
	{
		"type": "line text",
		"chapterNumber": 2,
		"verseNumber": 1,
		"sectionNumber": 3,
		"value": "My horn is exalted in Yahweh. "
	},
	{
		"type": "line break"
	},
	{
		"type": "line text",
		"chapterNumber": 2,
		"verseNumber": 1,
		"sectionNumber": 4,
		"value": "My mouth is enlarged over my enemies, "
	},
	{
		"type": "line break"
	},
	{
		"type": "line text",
		"chapterNumber": 2,
		"verseNumber": 1,
		"sectionNumber": 5,
		"value": "because I rejoice in your salvation. "
	},
	{
		"type": "line break"
	},
	{
		"type": "line text",
		"chapterNumber": 2,
		"verseNumber": 2,
		"sectionNumber": 1,
		"value": "There is no one as holy as Yahweh, "
	},
	{
		"type": "line break"
	},
	{
		"type": "line text",
		"chapterNumber": 2,
		"verseNumber": 2,
		"sectionNumber": 2,
		"value": "for there is no one besides you, "
	},
	{
		"type": "line break"
	},
	{
		"type": "line text",
		"chapterNumber": 2,
		"verseNumber": 2,
		"sectionNumber": 3,
		"value": "nor is there any rock like our God. "
	},
	{
		"type": "line break"
	},
	{
		"type": "stanza end"
	},
/* snip */
]
```

Object `type`s:

- paragraph start
- paragraph end
- paragraph text
- stanza start
- stanza end
- line text
- line break
- break

`line text` and `line break` will only occur between `stanza start` and `stanza end` objects.

`paragraph text` will only occur between `paragraph start` and `paragraph end` objects.
