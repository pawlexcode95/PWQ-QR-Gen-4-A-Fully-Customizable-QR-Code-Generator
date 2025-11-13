PWQ QR Gen 4 — A Fully Customizable QR Code Generator

PWQ QR Gen 4 is a powerful and flexible QR code generator built for developers, designers, and automation workflows. It supports all 40 QR versions, 8 mask patterns, 4 error correction levels, and every encoding mode, including Kanji and ECI (Extended Channel Interpretation).
✨ Key Features
• 	Full QR Spec Support: Encode using any version, mask, or error correction level.
• 	Advanced Encoding: Supports Byte, Alphanumeric, Numeric, Kanji, and ECI modes.
•   16 Diffrent Encoding Techniques: UTF-8, ISO-8859-1, ISO-8859-2 
•   Fully Customizable Grid of The QR Code: Color, Shape, Logo etc.
•   --- Dual-Mode Support -> Manual & PWQAI
•   Manual Mode: User enters parameters such as: version, mask, EC level, encoding etc. 
• 	PWQAI Mode: Automatically selects the optimal version and encoding parameters based on input data.
• 	--- Visual Customization:
• 	RGB foreground and background color control
• 	Circular or square grid modules
• 	Multi-logo support (Instagram, YouTube, WhatsApp, or custom uploads)
• 	Output Options: Save to PNG with custom filename and path
•   Very Simplistic Design & Usage

🧠 Built on Nayuki’s Logic
This project builds on the structural logic and segment division algorithms from Project Nayuki’s QR Code Generator, with extensive enhancements for customization and automation.

Usage Section
--- PWQAI Mode -> True
PWQQRGEN4 = PWQ_QR_GEN_4("これは漢字のエンコーディングの例です", <- Input Text
r"C:\Users\user\path\to\save", <- File path for saving
"PWQQRGen4_Example.png", <- File name + Format
(255, 0, 0), <-  Background color
(200, 200, 25),  <- Foreground color
gridshape="square", <- Shape of the grid | "square" or "circle"
logoimg="instagram", <- Logo embedded | "Instagram", "Youtube", "Whatsapp", "Paypal", "Netflix", "Messenger", "Gmail" or "None"
PWQAI_mode=True) <- PWQAI mode on 

--- PWQAI Mode -> False
PWQQRGEN4 = PWQ_QR_GEN_4("https://youtube.com", <- Input Text
r"C:\Users\user\path\to\save", <- File path for saving
"PWQQRGen4.png", <- File name + Format
(17, 18, 9), <-  Background color
(231, 90, 143), <- Foreground color
gridshape='circle', <- Shape of the grid | "square" or "circle"
gridsize=15, <- size of the module/individual grid in px
quietzonesize=6, <- size of the quiet zones/border in grid
logoimg='instagram', <- Logo embedded | "Instagram", "Youtube", "Whatsapp", "Paypal", "Netflix", "Messenger", "Gmail" or "None"
encoding="ISO-8859-1", <- Encoding Technique* see below
version=4,  <- Version size, range from 1 to 40, corresponds to 21x21 modules up to 177x177 modules
eclvl=PWQ_QR_GEN_4.PWQ_QR_Ecl._Quartile,  <- Error Correction Level | PWQ_QR_GEN_4.PWQ_QR_Ecl._Low, PWQ_QR_GEN_4.PWQ_QR_Ecl._Medium, PWQ_QR_GEN_4.PWQ_QR_Ecl._Quartile, PWQ_QR_GEN_4.PWQ_QR_Ecl._High
mask=0, <- Mask filter, ranges from 0 to 7, each 100% functional.
PWQAI_mode=False) <- PWQAI Mode off

--- Encoding Techqniues*
_ECI_Encoding_Table: dict[str, int] ={ # Table with 16 diffrent encoding techniques
    "ISO-8859-1": 3,       # Western European
    "ISO-8859-2": 4,       # Central European
    "ISO-8859-3": 5,       # South European
    "ISO-8859-4": 6,       # North European
    "ISO-8859-5": 7,       # Cyrillic
    "ISO-8859-6": 8,       # Arabic
    "ISO-8859-7": 9,       # Greek
    "ISO-8859-8": 10,      # Hebrew
    "ISO-8859-9": 11,      # Turkish
    "ISO-8859-13": 15,     # Baltic
    "ISO-8859-15": 17,     # Western European (Euro)
    "Shift_JIS": 20,       # Japanese
    "UTF-8": 26,           # Unicode (most common)
    "UTF-16BE": 28,        # Unicode Big Endian
    "UTF-16LE": 29,        # Unicode Little Endian
    "Windows-1252": 21     # Microsoft Western European (not officially in QR spec, but widely used)
    }
