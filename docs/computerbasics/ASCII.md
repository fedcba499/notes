## ASCII
ASCII stands for American Standard Code for Information Interchange. It is a 7-bit character code where each individual bit represents a unique character (0 - 127). Extended ASCII is a 8-bit table with  256 character and symbols. Extended ASCII includes all ASCII codes from standard ASCII.

> In C / C++ prefix is added to repesent HEX value, ex : 00 becomes 0x00, 0x01, 0x02 etc. 0x is prefix added to read it as HEX Value.

## HEX

Serial Communication happens 99% with SERIAL_8N1 configuration (8 bits data, No parity (No Checksum), 1 Stop bit). 8 bits makes 1 Byte Data. 

To represent value in Numeric System, it makes 256, because Numeric system is base 10. Which results in 3 digit number.what, if we use base 16 system, we can accomodate 256 options using two digits, that how HEX System born.

Using it is easier to represent byte data

```txt
01001000 01000101 01001100 01001100 01001111

48 45 4C 4C 4F

H  E  L  L  O
```

We dont use ASCII to represent Byte data because, we cannot remember 256 character. As we are familiar with Decimal system, we Use HEX as Extension of Decimal system.

## ASCII controll character (0 - 31)

unprintable control codes used to control peripherals.


| DEC | Binary        | HEX | Symbol | Description |
|-----|---------------|-----|--------|-------------|
| 0   | 00000000      | 00  | NUL    | Null |
| 1   | 00000001      | 01  | SOH    | Start of Heading |
| 2   | 00000010      | 02  | STX    | Start of Text |
| 3   | 00000011      | 03  | ETX    | End of Text |
| 4   | 00000100      | 04  | EOT    | End of Transmission |
| 5   | 00000101      | 05  | ENQ    | Enquiry |
| 6   | 00000110      | 06  | ACK    | Acknowledge |
| 7   | 00000111      | 07  | BEL    | Bell |
| 8   | 00001000      | 08  | BS     | Backspace |
| 9   | 00001001      | 09  | HT     | Horizontal Tab |
| 10  | 00001010      | 0A  | LF     | Line Feed |
| 11  | 00001011      | 0B  | VT     | Vertical Tab |
| 12  | 00001100      | 0C  | FF     | Form Feed |
| 13  | 00001101      | 0D  | CR     | Carriage Return |
| 14  | 00001110      | 0E  | SO     | Shift Out |
| 15  | 00001111      | 0F  | SI     | Shift In |
| 16  | 00010000      | 10  | DLE    | Data Link Escape |
| 17  | 00010001      | 11  | DC1    | Device Control 1 |
| 18  | 00010010      | 12  | DC2    | Device Control 2 |
| 19  | 00010011      | 13  | DC3    | Device Control 3 |
| 20  | 00010100      | 14  | DC4    | Device Control 4 |
| 21  | 00010101      | 15  | NAK    | Negative Acknowledge |
| 22  | 00010110      | 16  | SYN    | Synchronous Idle |
| 23  | 00010111      | 17  | ETB    | End of Transmission Block |
| 24  | 00011000      | 18  | CAN    | Cancel |
| 25  | 00011001      | 19  | EM     | End of Medium |
| 26  | 00011010      | 1A  | SUB    | Substitute |
| 27  | 00011011      | 1B  | ESC    | Escape |
| 28  | 00011100      | 1C  | FS     | File Separator |
| 29  | 00011101      | 1D  | GS     | Group Separator |
| 30  | 00011110      | 1E  | RS     | Record Separator |
| 31  | 00011111      | 1F  | US     | Unit Separator |

## ASCII Printable Character (32 - 127)

| DEC | Binary    | HEX | Symbol   | Description             |
|-----|-----------|-----|----------|-------------------------|
| 32  | 00100000  | 20  | (space)  | Space                   |
| 33  | 00100001  | 21  | !        | Exclamation Mark        |
| 34  | 00100010  | 22  | "        | Double Quote            |
| 35  | 00100011  | 23  | #        | Hash / Pound            |
| 36  | 00100100  | 24  | $        | Dollar Sign             |
| 37  | 00100101  | 25  | %        | Percent                 |
| 38  | 00100110  | 26  | &        | Ampersand               |
| 39  | 00100111  | 27  | '        | Single Quote            |
| 40  | 00101000  | 28  | (        | Left Parenthesis        |
| 41  | 00101001  | 29  | )        | Right Parenthesis       |
| 42  | 00101010  | 2A  | *        | Asterisk                |
| 43  | 00101011  | 2B  | +        | Plus                    |
| 44  | 00101100  | 2C  | ,        | Comma                   |
| 45  | 00101101  | 2D  | -        | Minus / Hyphen          |
| 46  | 00101110  | 2E  | .        | Period / Dot            |
| 47  | 00101111  | 2F  | /        | Slash                   |
| 48  | 00110000  | 30  | 0        | Digit 0                 |
| 49  | 00110001  | 31  | 1        | Digit 1                 |
| 50  | 00110010  | 32  | 2        | Digit 2                 |
| 51  | 00110011  | 33  | 3        | Digit 3                 |
| 52  | 00110100  | 34  | 4        | Digit 4                 |
| 53  | 00110101  | 35  | 5        | Digit 5                 |
| 54  | 00110110  | 36  | 6        | Digit 6                 |
| 55  | 00110111  | 37  | 7        | Digit 7                 |
| 56  | 00111000  | 38  | 8        | Digit 8                 |
| 57  | 00111001  | 39  | 9        | Digit 9                 |
| 58  | 00111010  | 3A  | :        | Colon                   |
| 59  | 00111011  | 3B  | ;        | Semicolon               |
| 60  | 00111100  | 3C  | <        | Less-than               |
| 61  | 00111101  | 3D  | =        | Equal Sign              |
| 62  | 00111110  | 3E  | >        | Greater-than            |
| 63  | 00111111  | 3F  | ?        | Question Mark           |
| 64  | 01000000  | 40  | @        | At Symbol               |
| 65  | 01000001  | 41  | A        | Uppercase A             |
| 66  | 01000010  | 42  | B        | Uppercase B             |
| 67  | 01000011  | 43  | C        | Uppercase C             |
| 68  | 01000100  | 44  | D        | Uppercase D             |
| 69  | 01000101  | 45  | E        | Uppercase E             |
| 70  | 01000110  | 46  | F        | Uppercase F             |
| 71  | 01000111  | 47  | G        | Uppercase G             |
| 72  | 01001000  | 48  | H        | Uppercase H             |
| 73  | 01001001  | 49  | I        | Uppercase I             |
| 74  | 01001010  | 4A  | J        | Uppercase J             |
| 75  | 01001011  | 4B  | K        | Uppercase K             |
| 76  | 01001100  | 4C  | L        | Uppercase L             |
| 77  | 01001101  | 4D  | M        | Uppercase M             |
| 78  | 01001110  | 4E  | N        | Uppercase N             |
| 79  | 01001111  | 4F  | O        | Uppercase O             |
| 80  | 01010000  | 50  | P        | Uppercase P             |
| 81  | 01010001  | 51  | Q        | Uppercase Q             |
| 82  | 01010010  | 52  | R        | Uppercase R             |
| 83  | 01010011  | 53  | S        | Uppercase S             |
| 84  | 01010100  | 54  | T        | Uppercase T             |
| 85  | 01010101  | 55  | U        | Uppercase U             |
| 86  | 01010110  | 56  | V        | Uppercase V             |
| 87  | 01010111  | 57  | W        | Uppercase W             |
| 88  | 01011000  | 58  | X        | Uppercase X             |
| 89  | 01011001  | 59  | Y        | Uppercase Y             |
| 90  | 01011010  | 5A  | Z        | Uppercase Z             |
| 91  | 01011011  | 5B  | [        | Left Square Bracket     |
| 92  | 01011100  | 5C  | \        | Backslash               |
| 93  | 01011101  | 5D  | ]        | Right Square Bracket    |
| 94  | 01011110  | 5E  | ^        | Caret                   |
| 95  | 01011111  | 5F  | _        | Underscore              |
| 96  | 01100000  | 60  | `        | Backtick                |
| 97  | 01100001  | 61  | a        | Lowercase a             |
| 98  | 01100010  | 62  | b        | Lowercase b             |
| 99  | 01100011  | 63  | c        | Lowercase c             |
|100  | 01100100  | 64  | d        | Lowercase d             |
|101  | 01100101  | 65  | e        | Lowercase e             |
|102  | 01100110  | 66  | f        | Lowercase f             |
|103  | 01100111  | 67  | g        | Lowercase g             |
|104  | 01101000  | 68  | h        | Lowercase h             |
|105  | 01101001  | 69  | i        | Lowercase i             |
|106  | 01101010  | 6A  | j        | Lowercase j             |
|107  | 01101011  | 6B  | k        | Lowercase k             |
|108  | 01101100  | 6C  | l        | Lowercase l             |
|109  | 01101101  | 6D  | m        | Lowercase m             |
|110  | 01101110  | 6E  | n        | Lowercase n             |
|111  | 01101111  | 6F  | o        | Lowercase o             |
|112  | 01110000  | 70  | p        | Lowercase p             |
|113  | 01110001  | 71  | q        | Lowercase q             |
|114  | 01110010  | 72  | r        | Lowercase r             |
|115  | 01110011  | 73  | s        | Lowercase s             |
|116  | 01110100  | 74  | t        | Lowercase t             |
|117  | 01110101  | 75  | u        | Lowercase u             |
|118  | 01110110  | 76  | v        | Lowercase v             |
|119  | 01110111  | 77  | w        | Lowercase w             |
|120  | 01111000  | 78  | x        | Lowercase x             |
|121  | 01111001  | 79  | y        | Lowercase y             |
|122  | 01111010  | 7A  | z        | Lowercase z             |
|123  | 01111011  | 7B  | {        | Left Curly Brace        |
|124  | 01111100  | 7C  | \|       | Vertical Bar / Pipe     |
|125  | 01111101  | 7D  | }        | Right Curly Brace       |
|126  | 01111110  | 7E  | ~        | Tilde                   |
|127  | 01111111  | 7F  | DEL      | Delete                  |

## Extended ASCII codes (character code 128 - 255)

| DEC | Binary    | HEX | Symbol | Description |
|-----|-----------|-----|--------|-------------|
|128 | 10000000 | 80 | € | Euro Sign |
|129 | 10000001 | 81 |     | (unused) |
|130 | 10000010 | 82 | ‚ | Single Low-9 Quote |
|131 | 10000011 | 83 | ƒ | Latin Small Letter F with Hook |
|132 | 10000100 | 84 | „ | Double Low-9 Quote |
|133 | 10000101 | 85 | … | Ellipsis |
|134 | 10000110 | 86 | † | Dagger |
|135 | 10000111 | 87 | ‡ | Double Dagger |
|136 | 10001000 | 88 | ˆ | Modifier Circumflex |
|137 | 10001001 | 89 | ‰ | Per Mille |
|138 | 10001010 | 8A | Š | Latin Capital S with Caron |
|139 | 10001011 | 8B | ‹ | Single Left-Pointing Quote |
|140 | 10001100 | 8C | Œ | Latin Capital Ligature OE |
|141 | 10001101 | 8D |     | (unused) |
|142 | 10001110 | 8E | Ž | Latin Capital Z with Caron |
|143 | 10001111 | 8F |     | (unused) |
|144 | 10010000 | 90 |     | (unused) |
|145 | 10010001 | 91 | ‘ | Left Single Quote |
|146 | 10010010 | 92 | ’ | Right Single Quote |
|147 | 10010011 | 93 | “ | Left Double Quote |
|148 | 10010100 | 94 | ” | Right Double Quote |
|149 | 10010101 | 95 | • | Bullet |
|150 | 10010110 | 96 | – | En Dash |
|151 | 10010111 | 97 | — | Em Dash |
|152 | 10011000 | 98 | ˜ | Small Tilde |
|153 | 10011001 | 99 | ™ | Trademark |
|154 | 10011010 | 9A | š | Latin Small S with Caron |
|155 | 10011011 | 9B | › | Single Right Quote |
|156 | 10011100 | 9C | œ | Latin Small Ligature OE |
|157 | 10011101 | 9D |     | (unused) |
|158 | 10011110 | 9E | ž | Latin Small Z with Caron |
|159 | 10011111 | 9F | Ÿ | Latin Capital Y with Diaeresis |
|160 | 10100000 | A0 |   | Non-Breaking Space |
|161 | 10100001 | A1 | ¡ | Inverted Exclamation |
|162 | 10100010 | A2 | ¢ | Cent |
|163 | 10100011 | A3 | £ | Pound |
|164 | 10100100 | A4 | ¤ | Currency |
|165 | 10100101 | A5 | ¥ | Yen |
|166 | 10100110 | A6 | ¦ | Broken Bar |
|167 | 10100111 | A7 | § | Section |
|168 | 10101000 | A8 | ¨ | Diaeresis |
|169 | 10101001 | A9 | © | Copyright |
|170 | 10101010 | AA | ª | Feminine Ordinal |
|171 | 10101011 | AB | « | Left Angle Quote |
|172 | 10101100 | AC | ¬ | Not Sign |
|173 | 10101101 | AD | ­ | Soft Hyphen |
|174 | 10101110 | AE | ® | Registered |
|175 | 10101111 | AF | ¯ | Macron |
|176 | 10110000 | B0 | ° | Degree |
|177 | 10110001 | B1 | ± | Plus-Minus |
|178 | 10110010 | B2 | ² | Superscript 2 |
|179 | 10110011 | B3 | ³ | Superscript 3 |
|180 | 10110100 | B4 | ´ | Acute Accent |
|181 | 10110101 | B5 | µ | Micro Sign |
|182 | 10110110 | B6 | ¶ | Pilcrow |
|183 | 10110111 | B7 | · | Middle Dot |
|184 | 10111000 | B8 | ¸ | Cedilla |
|185 | 10111001 | B9 | ¹ | Superscript 1 |
|186 | 10111010 | BA | º | Masculine Ordinal |
|187 | 10111011 | BB | » | Right Angle Quote |
|188 | 10111100 | BC | ¼ | One Quarter |
|189 | 10111101 | BD | ½ | One Half |
|190 | 10111110 | BE | ¾ | Three Quarters |
|191 | 10111111 | BF | ¿ | Inverted Question |
|192 | 11000000 | C0 | À | A Grave |
|193 | 11000001 | C1 | Á | A Acute |
|194 | 11000010 | C2 | Â | A Circumflex |
|195 | 11000011 | C3 | Ã | A Tilde |
|196 | 11000100 | C4 | Ä | A Umlaut |
|197 | 11000101 | C5 | Å | A Ring |
|198 | 11000110 | C6 | Æ | AE |
|199 | 11000111 | C7 | Ç | C Cedilla |
|200 | 11001000 | C8 | È | E Grave |
|201 | 11001001 | C9 | É | E Acute |
|202 | 11001010 | CA | Ê | E Circumflex |
|203 | 11001011 | CB | Ë | E Umlaut |
|204 | 11001100 | CC | Ì | I Grave |
|205 | 11001101 | CD | Í | I Acute |
|206 | 11001110 | CE | Î | I Circumflex |
|207 | 11001111 | CF | Ï | I Umlaut |
|208 | 11010000 | D0 | Ð | Eth |
|209 | 11010001 | D1 | Ñ | N Tilde |
|210 | 11010010 | D2 | Ò | O Grave |
|211 | 11010011 | D3 | Ó | O Acute |
|212 | 11010100 | D4 | Ô | O Circumflex |
|213 | 11010101 | D5 | Õ | O Tilde |
|214 | 11010110 | D6 | Ö | O Umlaut |
|215 | 11010111 | D7 | × | Multiplication |
|216 | 11011000 | D8 | Ø | O Slash |
|217 | 11011001 | D9 | Ù | U Grave |
|218 | 11011010 | DA | Ú | U Acute |
|219 | 11011011 | DB | Û | U Circumflex |
|220 | 11011000 | DC | Ü | U Umlaut |
|221 | 11011101 | DD | Ý | Y Acute |
|222 | 11011110 | DE | Þ | Thorn |
|223 | 11011111 | DF | ß | Sharp S (Eszett) |
|224 | 11100000 | E0 | à | a Grave |
|225 | 11100001 | E1 | á | a Acute |
|226 | 11100010 | E2 | â | a Circumflex |
|227 | 11100011 | E3 | ã | a Tilde |
|228 | 11100100 | E4 | ä | a Umlaut |
|229 | 11100101 | E5 | å | a Ring |
|230 | 11100110 | E6 | æ | ae |
|231 | 11100111 | E7 | ç | c Cedilla |
|232 | 11101000 | E8 | è | e Grave |
|233 | 11101001 | E9 | é | e Acute |
|234 | 11101010 | EA | ê | e Circumflex |
|235 | 11101011 | EB | ë | e Umlaut |
|236 | 11101100 | EC | ì | i Grave |
|237 | 11101101 | ED | í | i Acute |
|238 | 11101110 | EE | î | i Circumflex |
|239 | 11101111 | EF | ï | i Umlaut |
|240 | 11110000 | F0 | ð | Eth |
|241 | 11110001 | F1 | ñ | n Tilde |
|242 | 11110010 | F2 | ò | o Grave |
|243 | 11110011 | F3 | ó | o Acute |
|244 | 11110100 | F4 | ô | o Circumflex |
|245 | 11110101 | F5 | õ | o Tilde |
|246 | 11110110 | F6 | ö | o Umlaut |
|247 | 11110111 | F7 | ÷ | Division |
|248 | 11111000 | F8 | ø | o Slash |
|249 | 11111001 | F9 | ù | u Grave |
|250 | 11111010 | FA | ú | u Acute |
|251 | 11111011 | FB | û | u Circumflex |
|252 | 11111100 | FC | ü | u Umlaut |
|253 | 11111101 | FD | ý | y Acute |
|254 | 11111110 | FE | þ | Thorn |
|255 | 11111111 | FF | ÿ | y Umlaut |


