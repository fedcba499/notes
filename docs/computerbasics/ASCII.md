## ASCII
ASCII stands for American Standard Code for Information Interchange. It is a 7-bit character code where each individual bit represents a unique character (0 - 127). Extended ASCII is a 8-bit table with  256 character and symbols. Extended ASCII includes all ASCII codes from standard ASCII.

> In C / C++ prefix is added to repesent HEX value, ex : 00 becomes 0x00, 0x01, 0x02 etc. 0x is prefix added to read it as HEX Value.

## ASCII controll character (0 - 31)
unprintable control codes used to control peripherals.

| DEC | HEX | Symbol | Description |
| --- | --- | --- | --- |
| 0   | 00  | NUL  | Null |
| 1   | 01  | SOH  | Start of Heading |
| 2   | 02  | STX  | Start of Text |
| 3   | 03  | ETX  | End of Text |
| 4   | 04  | EOT  | End of Transmission |
| 5   | 05  | ENQ  | Enquiry |
| 6   | 06  | ACK  | Acknowledge |
| 7   | 07  | BEL  | Bell |
| 8   | 08  | BS   | Backspace |
| 9   | 09  | HT   | Horizontal Tab |
| 10  | 0A  | LF   | Line Feed |
| 11  | 0B  | VT   | Vertical Tab |
| 12  | 0C  | FF   | Form Feed |
| 13  | 0D  | CR   | Carriage Return |
| 14  | 0E  | SO   | Shift Out |
| 15  | 0F  | SI   | Shift In |
| 16  | 10  | DLE  | Data Link Escape |
| 17  | 11  | DC1  | Device Control 1 |
| 18  | 12  | DC2  | Device Control 2 |
| 19  | 13  | DC3  | Device Control 3 |
| 20  | 14  | DC4  | Device Control 4 |
| 21  | 15  | NAK  | Negative Acknowledge |
| 22  | 16  | SYN  | Synchronous Idle |
| 23  | 17  | ETB  | End of Transmission Block |
| 24  | 18  | CAN  | Cancel |
| 25  | 19  | EM   | End of Medium |
| 26  | 1A  | SUB  | Substitute |
| 27  | 1B  | ESC  | Escape |
| 28  | 1C  | FS   | File Separator |
| 29  | 1D  | GS   | Group Separator |
| 30  | 1E  | RS   | Record Separator |
| 31  | 1F  | US   | Unit Separator |

## ASCII Printable Character (32 - 127)

| DEC | HEX | Symbol | Description |
| --- | --- | --- | --- |
| 32  | 20  | (space) | Space |
| 33  | 21  | !    | Exclamation |
| 34  | 22  | "    | Double Quote |
| 35  | 23  | #    | Hash |
| 36  | 24  | $    | Dollar |
| 37  | 25  | %    | Percent |
| 38  | 26  | &    | Ampersand |
| 39  | 27  | '    | Single Quote |
| 40  | 28  | (    | Left Parenthesis |
| 41  | 29  | )    | Right Parenthesis |
| 42  | 2A  | *    | Asterisk |
| 43  | 2B  | +    | Plus |
| 44  | 2C  | ,    | Comma |
| 45  | 2D  | -    | Minus |
| 46  | 2E  | .    | Period |
| 47  | 2F  | /    | Slash |
| 48  | 30  | 0    | Digit 0 |
| 49  | 31  | 1    | Digit 1 |
| 50  | 32  | 2    | Digit 2 |
| 51  | 33  | 3    | Digit 3 |
| 52  | 34  | 4    | Digit 4 |
| 53  | 35  | 5    | Digit 5 |
| 54  | 36  | 6    | Digit 6 |
| 55  | 37  | 7    | Digit 7 |
| 56  | 38  | 8    | Digit 8 |
| 57  | 39  | 9    | Digit 9 |
| 58  | 3A  | :    | Colon |
| 59  | 3B  | ;    | Semicolon |
| 60  | 3C  | <    | Less Than |
| 61  | 3D  | =    | Equal |
| 62  | 3E  | >    | Greater Than |
| 63  | 3F  | ?    | Question Mark |
| 64  | 40  | @    | At |
| 65  | 41  | A    | Uppercase A |
| 66  | 42  | B    | Uppercase B |
| 67  | 43  | C    | Uppercase C |
| 68  | 44  | D    | Uppercase D |
| 69  | 45  | E    | Uppercase E |
| 70  | 46  | F    | Uppercase F |
| 71  | 47  | G    | Uppercase G |
| 72  | 48  | H    | Uppercase H |
| 73  | 49  | I    | Uppercase I |
| 74  | 4A  | J    | Uppercase J |
| 75  | 4B  | K    | Uppercase K |
| 76  | 4C  | L    | Uppercase L |
| 77  | 4D  | M    | Uppercase M |
| 78  | 4E  | N    | Uppercase N |
| 79  | 4F  | O    | Uppercase O |
| 80  | 50  | P    | Uppercase P |
| 81  | 51  | Q    | Uppercase Q |
| 82  | 52  | R    | Uppercase R |
| 83  | 53  | S    | Uppercase S |
| 84  | 54  | T    | Uppercase T |
| 85  | 55  | U    | Uppercase U |
| 86  | 56  | V    | Uppercase V |
| 87  | 57  | W    | Uppercase W |
| 88  | 58  | X    | Uppercase X |
| 89  | 59  | Y    | Uppercase Y |
| 90  | 5A  | Z    | Uppercase Z |
| 91  | 5B  | [    | Left Bracket |
| 92  | 5C  | \    | Backslash |
| 93  | 5D  | ]    | Right Bracket |
| 94  | 5E  | ^    | Caret |
| 95  | 5F  | _    | Underscore |
| 96  | 60  | `    | Backtick |
| 97  | 61  | a    | Lowercase a |
| 98  | 62  | b    | Lowercase b |
| 99  | 63  | c    | Lowercase c |
| 100 | 64  | d    | Lowercase d |
| 101 | 65  | e    | Lowercase e |
| 102 | 66  | f    | Lowercase f |
| 103 | 67  | g    | Lowercase g |
| 104 | 68  | h    | Lowercase h |
| 105 | 69  | i    | Lowercase i |
| 106 | 6A  | j    | Lowercase j |
| 107 | 6B  | k    | Lowercase k |
| 108 | 6C  | l    | Lowercase l |
| 109 | 6D  | m    | Lowercase m |
| 110 | 6E  | n    | Lowercase n |
| 111 | 6F  | o    | Lowercase o |
| 112 | 70  | p    | Lowercase p |
| 113 | 71  | q    | Lowercase q |
| 114 | 72  | r    | Lowercase r |
| 115 | 73  | s    | Lowercase s |
| 116 | 74  | t    | Lowercase t |
| 117 | 75  | u    | Lowercase u |
| 118 | 76  | v    | Lowercase v |
| 119 | 77  | w    | Lowercase w |
| 120 | 78  | x    | Lowercase x |
| 121 | 79  | y    | Lowercase y |
| 122 | 7A  | z    | Lowercase z |
| 123 | 7B  | {    | Left Brace |
| 124 | 7C  | |    | Vertical Bar |
| 125 | 7D  | }    | Right Brace |
| 126 | 7E  | ~    | Tilde |
| 127 | 7F  | DEL  | Delete |

## Extended ASCII codes (character code 128 - 255)

| DEC | HEX | Symbol | Description |
| --- | --- | --- | --- |
| 128 | 80  | € | Euro Sign |
| 129 | 81  |   | (unused) |
| 130 | 82  | ‚ | Single Low Quote |
| 131 | 83  | ƒ | Florin |
| 132 | 84  | „ | Double Low Quote |
| 133 | 85  | … | Ellipsis |
| 134 | 86  | † | Dagger |
| 135 | 87  | ‡ | Double Dagger |
| 136 | 88  | ˆ | Circumflex |
| 137 | 89  | ‰ | Per Mille |
| 138 | 8A  | Š | S with Caron |
| 139 | 8B  | ‹ | Single Left Angle |
| 140 | 8C  | Œ | OE Ligature |
| 141 | 8D  |   | (unused) |
| 142 | 8E  | Ž | Z with Caron |
| 143 | 8F  |   | (unused) |
| 144 | 90  |   | (unused) |
| 145 | 91  | ‘ | Left Single Quote |
| 146 | 92  | ’ | Right Single Quote |
| 147 | 93  | “ | Left Double Quote |
| 148 | 94  | ” | Right Double Quote |
| 149 | 95  | • | Bullet |
| 150 | 96  | – | En Dash |
| 151 | 97  | — | Em Dash |
| 152 | 98  | ˜ | Small Tilde |
| 153 | 99  | ™ | Trademark |
| 154 | 9A  | š | s with Caron |
| 155 | 9B  | › | Single Right Angle |
| 156 | 9C  | œ | oe |
| 157 | 9D  |   | (unused) |
| 158 | 9E  | ž | z with Caron |
| 159 | 9F  | Ÿ | Y with Diaeresis |
| 160 | A0  |   | Non-breaking Space |
| 161 | A1  | ¡ | Inverted Exclamation |
| 162 | A2  | ¢ | Cent |
| 163 | A3  | £ | Pound |
| 164 | A4  | ¤ | Currency |
| 165 | A5  | ¥ | Yen |
| 166 | A6  | ¦ | Broken Bar |
| 167 | A7  | § | Section |
| 168 | A8  | ¨ | Diaeresis |
| 169 | A9  | © | Copyright |
| 170 | AA  | ª | Feminine Ordinal |
| 171 | AB  | « | Left Angle Quote |
| 172 | AC  | ¬ | Not Sign |
| 173 | AD  | ­ | Soft Hyphen |
| 174 | AE  | ® | Registered |
| 175 | AF  | ¯ | Macron |
| 176 | B0  | ° | Degree |
| 177 | B1  | ± | Plus Minus |
| 178 | B2  | ² | Superscript 2 |
| 179 | B3  | ³ | Superscript 3 |
| 180 | B4  | ´ | Acute Accent |
| 181 | B5  | µ | Micro Sign |
| 182 | B6  | ¶ | Pilcrow |
| 183 | B7  | · | Middle Dot |
| 184 | B8  | ¸ | Cedilla |
| 185 | B9  | ¹ | Superscript 1 |
| 186 | BA  | º | Masculine Ordinal |
| 187 | BB  | » | Right Angle Quote |
| 188 | BC  | ¼ | One Quarter |
| 189 | BD  | ½ | One Half |
| 190 | BE  | ¾ | Three Quarters |
| 191 | BF  | ¿ | Inverted Question |
| 192 | C0  | À | A Grave |
| 193 | C1  | Á | A Acute |
| 194 | C2  | Â | A Circumflex |
| 195 | C3  | Ã | A Tilde |
| 196 | C4  | Ä | A Umlaut |
| 197 | C5  | Å | A Ring |
| 198 | C6  | Æ | AE |
| 199 | C7  | Ç | C Cedilla |
| 200 | C8  | È | E Grave |
| 201 | C9  | É | E Acute |
| 202 | CA  | Ê | E Circumflex |
| 203 | CB  | Ë | E Diaeresis |
| 204 | CC  | Ì | I Grave |
| 205 | CD  | Í | I Acute |
| 206 | CE  | Î | I Circumflex |
| 207 | CF  | Ï | I Diaeresis |
| 208 | D0  | Ð | Eth |
| 209 | D1  | Ñ | N Tilde |
| 210 | D2  | Ò | O Grave |
| 211 | D3  | Ó | O Acute |
| 212 | D4  | Ô | O Circumflex |
| 213 | D5  | Õ | O Tilde |
| 214 | D6  | Ö | O Diaeresis |
| 215 | D7  | × | Multiply |
| 216 | D8  | Ø | O Slash |
| 217 | D9  | Ù | U Grave |
| 218 | DA  | Ú | U Acute |
| 219 | DB  | Û | U Circumflex |
| 220 | DC  | Ü | U Diaeresis |
| 221 | DD  | Ý | Y Acute |
| 222 | DE  | Þ | Thorn |
| 223 | DF  | ß | Sharp s |
| 224 | E0  | à | a Grave |
| 225 | E1  | á | a Acute |
| 226 | E2  | â | a Circumflex |
| 227 | E3  | ã | a Tilde |
| 228 | E4  | ä | a Diaeresis |
| 229 | E5  | å | a Ring |
| 230 | E6  | æ | ae |
| 231 | E7  | ç | c Cedilla |
| 232 | E8  | è | e Grave |
| 233 | E9  | é | e Acute |
| 234 | EA  | ê | e Circumflex |
| 235 | EB  | ë | e Diaeresis |
| 236 | EC  | ì | i Grave |
| 237 | ED  | í | i Acute |
| 238 | EE  | î | i Circumflex |
| 239 | EF  | ï | i Diaeresis |
| 240 | F0  | ð | Eth small |
| 241 | F1  | ñ | n Tilde |
| 242 | F2  | ò | o Grave |
| 243 | F3  | ó | o Acute |
| 244 | F4  | ô | o Circumflex |
| 245 | F5  | õ | o Tilde |
| 246 | F6  | ö | o Diaeresis |
| 247 | F7  | ÷ | Division |
| 248 | F8  | ø | o Slash |
| 249 | F9  | ù | u Grave |
| 250 | FA  | ú | u Acute |
| 251 | FB  | û | u Circumflex |
| 252 | FC  | ü | u Diaeresis |
| 253 | FD  | ý | y Acute |
| 254 | FE  | þ | Thorn small |
| 255 | FF  | ÿ | y Diaeresis |

