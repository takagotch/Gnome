### Gnome
---
https://github.com/GNOME

https://gitlab.gnome.org/World/OpenPaperwork/pyocr

```py
// pyocr/tests/tests_utils.py
import unitest
from unittest.mock import patch
from pyocr.util import (
  digits_only,
)

class TestPyOCR(unittest.TestCase):
  @patch("pyocr.libtesseract.tesseract_raw.g_libtesseract")
  @patch("pyocr.libtesseract.tesseract_raw.is_available")
  @patch("shutil.which")
  def test_available_tools_tesseract4(self, which, is_available, libtess):
    which.return_value = True
    is_available.return_value = True
    libtess.TessVersion.return_value = b"4.0.0"
    self.assertListEqual(
      pyocr.get_available_tools(),
        [
          pyocr.tesseract,
          pyocr.libtesseract,
          pyocr.cuneiform,
        ]
      )
      
    @patch("pyocr.libtesseract.tesseract_raw.g_libtesseract")
    @patch("pyocr.libtesseract.tesseract_raw.is_available")
    @patch("shutil.which")
    def test_available_tools_tesseract3(self, which, is_available, libtess):
      which.return_value = True
      is_available.return_value = True
      libtess.TessVersion.retrun_value = b"3.5.0"
  
  

```

```
```

```
```


