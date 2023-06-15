# Technical 6

## Case
Negara-negara yang mengikuti FIFA World Cup 2022 dibagi menjadi 8 group. Untuk bisa lolos ke babak selanjutnya (16 besar) diambil perwakilan 2 negara dengan poin tertinggi dari masing-masing group.

Data hasil dari seluruh pertandingan di fase group sudah dicatat di dengan format JSON di seperti contoh dibawah.
Negara mana sajakah yang lolos ke babak 16 besar? Buatlah sebuah program untuk menampilkan negara-negara yang lolos ke babak 16 besar.

Penentuan poin sebagai berikut:
- Jika menang (win), tim mendapatkan 3 poin
- Jika seri (draw), tim mendapatkan 1 poin
- Jika kalah (lose), tim mendapatkan poin 0

## Source Data
```json
[
	{
		"name": "Netherlands",
		"group": "A",
		"matches": [
			{ "against": "Senegal", "result": "win" },
			{ "against": "Ecuador", "result": "draw" },
			{ "against": "Qatar", "result": "win" }
		]
	},
	{
		"name": "Senegal",
		"group": "A",
		"matches": [
			{ "against": "Netherlands", "result": "lose" },
			{ "against": "Qatar", "result": "win" },
			{ "against": "Ecuador", "result": "win" }
		]
	},
	{
		"name": "Ecuador",
		"group": "A",
		"matches": [
			{ "against": "Qatar", "result": "win" },
			{ "against": "Netherlands", "result": "draw" },
			{ "against": "Senegal", "result": "lose" }
		]
	},
	{
		"name": "Qatar",
		"group": "A",
		"matches": [
			{ "against": "Ecuador", "result": "lose" },
			{ "against": "Senegal", "result": "lose" },
			{ "against": "Netherlands", "result": "lose" }
		]
	},
	{
		"name": "England",
		"group": "B",
		"matches": [
			{ "against": "Iran", "result": "win" },
			{ "against": "USA", "result": "draw" },
			{ "against": "Wales", "result": "win" }
		]
	},
	{
		"name": "USA",
		"group": "B",
		"matches": [
			{ "against": "Wales", "result": "draw" },
			{ "against": "England", "result": "draw" },
			{ "against": "Iran", "result": "win" }
		]
	},
	{
		"name": "Iran",
		"group": "B",
		"matches": [
			{ "against": "England", "result": "lose" },
			{ "against": "Wales", "result": "win" },
			{ "against": "USA", "result": "lose" }
		]
	},
	{
		"name": "Wales",
		"group": "B",
		"matches": [
			{ "against": "USA", "result": "draw" },
			{ "against": "Iran", "result": "lose" },
			{ "against": "England", "result": "lose" }
		]
	},
	{
		"name": "Argentina",
		"group": "C",
		"matches": [
			{ "against": "Saudi Arabia", "result": "lose" },
			{ "against": "Mexico", "result": "win" },
			{ "against": "Poland", "result": "win" }
		]
	},
	{
		"name": "Poland",
		"group": "C",
		"matches": [
			{ "against": "Mexico", "result": "draw" },
			{ "against": "Saudi Arabia", "result": "win" },
			{ "against": "Argentina", "result": "lose" }
		]
	},
	{
		"name": "Mexico",
		"group": "C",
		"matches": [
			{ "against": "Poland", "result": "draw" },
			{ "against": "Argentina", "result": "lose" },
			{ "against": "Saudi Arabia", "result": "win" }
		]
	},
	{
		"name": "Saudi Arabia",
		"group": "C",
		"matches": [
			{ "against": "Argentina", "result": "win" },
			{ "against": "Poland", "result": "lose" },
			{ "against": "Mexico", "result": "lose" }
		]
	},
	{
		"name": "France",
		"group": "D",
		"matches": [
			{ "against": "Australia", "result": "win" },
			{ "against": "Denmark", "result": "win" },
			{ "against": "Tunisia", "result": "lose" }
		]
	},
	{
		"name": "Australia",
		"group": "D",
		"matches": [
			{ "against": "France", "result": "lose" },
			{ "against": "Tunisia", "result": "win" },
			{ "against": "Denmark", "result": "win" }
		]
	},
	{
		"name": "Tunisia",
		"group": "D",
		"matches": [
			{ "against": "Denmark", "result": "draw" },
			{ "against": "Australia", "result": "lose" },
			{ "against": "France", "result": "win" }
		]
	},
	{
		"name": "Denmark",
		"group": "D",
		"matches": [
			{ "against": "Tunisia", "result": "draw" },
			{ "against": "France", "result": "lose" },
			{ "against": "Australia", "result": "lose" }
		]
	},
	{
		"name": "Japan",
		"group": "E",
		"matches": [
			{ "against": "Germany", "result": "win" },
			{ "against": "Costa Rica", "result": "lose" },
			{ "against": "Spain", "result": "win" }
		]
	},
	{
		"name": "Spain",
		"group": "E",
		"matches": [
			{ "against": "Costa Rica", "result": "win" },
			{ "against": "Germany", "result": "draw" },
			{ "against": "Japan", "result": "lose" }
		]
	},
	{
		"name": "Germany",
		"group": "E",
		"matches": [
			{ "against": "Japan", "result": "lose" },
			{ "against": "Spain", "result": "draw" },
			{ "against": "Costa Rica", "result": "win" }
		]
	},
	{
		"name": "Costa Rica",
		"group": "E",
		"matches": [
			{ "against": "Spain", "result": "lose" },
			{ "against": "Japan", "result": "win" },
			{ "against": "Germany", "result": "lose" }
		]
	},
	{
		"name": "Morocco",
		"group": "F",
		"matches": [
			{ "against": "Croatia", "result": "draw" },
			{ "against": "Belgium", "result": "win" },
			{ "against": "Canada", "result": "win" }
		]
	},
	{
		"name": "Croatia",
		"group": "F",
		"matches": [
			{ "against": "Morocco", "result": "draw" },
			{ "against": "Canada", "result": "win" },
			{ "against": "Belgium", "result": "draw" }
		]
	},
	{
		"name": "Belgium",
		"group": "F",
		"matches": [
			{ "against": "Canada", "result": "win" },
			{ "against": "Morocco", "result": "lose" },
			{ "against": "Croatia", "result": "draw" }
		]
	},
	{
		"name": "Canada",
		"group": "F",
		"matches": [
			{ "against": "Belgium", "result": "lose" },
			{ "against": "Croatia", "result": "lose" },
			{ "against": "Morocco", "result": "lose" }
		]
	},
	{
		"name": "Brazil",
		"group": "G",
		"matches": [
			{ "against": "Serbia", "result": "win" },
			{ "against": "Switzerland", "result": "win" },
			{ "against": "Cameroon", "result": "lose" }
		]
	},
	{
		"name": "Switzerland",
		"group": "G",
		"matches": [
			{ "against": "Cameroon", "result": "win" },
			{ "against": "Brazil", "result": "lose" },
			{ "against": "Serbia", "result": "win" }
		]
	},
	{
		"name": "Cameroon",
		"group": "G",
		"matches": [
			{ "against": "Switzerland", "result": "lose" },
			{ "against": "Serbia", "result": "draw" },
			{ "against": "Brazil", "result": "win" }
		]
	},
	{
		"name": "Serbia",
		"group": "G",
		"matches": [
			{ "against": "Brazil", "result": "lose" },
			{ "against": "Cameroon", "result": "draw" },
			{ "against": "Switzerland", "result": "lose" }
		]
	},
	{
		"name": "Portugal",
		"group": "H",
		"matches": [
			{ "against": "Ghana", "result": "win" },
			{ "against": "Uruguay", "result": "win" },
			{ "against": "South Korea", "result": "lose" }
		]
	},
	{
		"name": "South Korea",
		"group": "H",
		"matches": [
			{ "against": "Uruguay", "result": "draw" },
			{ "against": "Ghana", "result": "lose" },
			{ "against": "Portugal", "result": "win" }
		]
	},
	{
		"name": "Uruguay",
		"group": "H",
		"matches": [
			{ "against": "South Korea", "result": "draw" },
			{ "against": "Portugal", "result": "lose" },
			{ "against": "Ghana", "result": "win" }
		]
	},
	{
		"name": "Ghana",
		"group": "H",
		"matches": [
			{ "against": "Portugal", "result": "lose" },
			{ "against": "South Korea", "result": "win" },
			{ "against": "Uruguay", "result": "lose" }
		]
	}
]
```

## Output

```json
[ { name: "Indonesia", group: "Y", match_played: 3, points: 0 } ]
```