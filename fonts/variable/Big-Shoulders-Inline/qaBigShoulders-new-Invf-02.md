## Fontbakery report

Fontbakery version: 0.7.34

<details>
<summary><b>[7] BigShouldersInline[opsz,wght].ttf</b></summary>
<details>
<summary>🔥 <b>FAIL:</b> Validate STAT particle names and values match the fallback names in GFAxisRegistry. </summary>

* [com.google.fonts/check/STAT/gf-axisregistry](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/STAT/gf-axisregistry)
<pre>--- Rationale ---

Check that particle names and values on STAT table match the fallback names in
each axis entry at the Google Fonts Axis Registry, available at
https://github.com/google/fonts/tree/master/axisregistry


</pre>

* 🔥 **FAIL** On the font variation axis 'opsz', the name 'Display' is not among the expected ones (6pt, 7pt, 8pt, 9pt, 10pt, 11pt, 12pt, 14pt, 16pt, 18pt, 20pt, 24pt, 28pt, 36pt, 48pt, 60pt, 72pt, 96pt, 120pt, 144pt) according to the Google Fonts Axis Registry. [code: invalid-name]
* 🔥 **FAIL** On the font variation axis 'opsz', the name 'Text' is not among the expected ones (6pt, 7pt, 8pt, 9pt, 10pt, 11pt, 12pt, 14pt, 16pt, 18pt, 20pt, 24pt, 28pt, 36pt, 48pt, 60pt, 72pt, 96pt, 120pt, 144pt) according to the Google Fonts Axis Registry. [code: invalid-name]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check glyphs do not have components which are themselves components.</summary>

* [com.google.fonts/check/glyf_nested_components](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/glyf.html#com.google.fonts/check/glyf_nested_components)
<pre>--- Rationale ---

There have been bugs rendering variable fonts with nested components.
Additionally, some static fonts with nested components have been reported to
have rendering and printing issues.

For more info, see:
* https://github.com/googlefonts/fontbakery/issues/2961
* https://github.com/arrowtype/recursive/issues/412


</pre>

* 🔥 **FAIL** The following glyphs have components which themselves are component glyphs:
	* uni1EAE
	* uni1EB0
	* uni1EB2
	* uni1EB4
	* uni1EA4
	* uni1EA6
	* uni1EA8
	* uni1EAA
	* uni0202
	* uni1E08 and 117 more. [code: found-nested-components]

</details>
<details>
<summary>⚠ <b>WARN:</b> Stricter unitsPerEm criteria for Google Fonts. </summary>

* [com.google.fonts/check/unitsperem_strict](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/unitsperem_strict)
<pre>--- Rationale ---

Even though the OpenType spec allows unitsPerEm to be any value between 16 and
16384, the Google Fonts project aims at a narrower set of reasonable values.

The spec suggests usage of powers of two in order to get some performance
improvements on legacy renderers, so those values are acceptable.

But values of 500 or 1000 are also acceptable, with the added benefit that it
makes upm math easier for designers, while the performance hit of not using a
power of two is most likely negligible nowadays.

Additionally, values above 2048 would likely result in unreasonable filesize
increases.


</pre>

* ⚠ **WARN** Font em size (unitsPerEm) is 4000 which may be too large (causing filesize bloat), unless you are sure that the detail level in this font requires that much precision. [code: large-value]

</details>
<details>
<summary>⚠ <b>WARN:</b> Is there kerning info for non-ligated sequences?</summary>

* [com.google.fonts/check/kerning_for_non_ligated_sequences](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/kerning_for_non_ligated_sequences)
<pre>--- Rationale ---

Fonts with ligatures should have kerning on the corresponding non-ligated
sequences for text where ligatures aren&#x27;t used (eg
https://github.com/impallari/Raleway/issues/14).


</pre>

* ⚠ **WARN** GPOS table lacks kerning info for the following non-ligated sequences:
	- f + f
	- f + i
	- i + f
	- f + l
	- l + f
	- i + l

   [code: lacks-kern-info]

</details>
<details>
<summary>⚠ <b>WARN:</b> Combined length of family and style must not exceed 27 characters.</summary>

* [com.google.fonts/check/name/family_and_style_max_length](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/name/family_and_style_max_length)
<pre>--- Rationale ---

According to a GlyphsApp tutorial [1], in order to make sure all versions of
Windows recognize it as a valid font file, we must make sure that the
concatenated length of the familyname (NameID.FONT_FAMILY_NAME) and style
(NameID.FONT_SUBFAMILY_NAME) strings in the name table do not exceed 20
characters.

After discussing the problem in more detail at `FontBakery issue #2179 [2] we
decided that allowing up to 27 chars would still be on the safe side, though.

[1]
https://glyphsapp.com/tutorials/multiple-masters-part-3-setting-up-instances
[2] https://github.com/googlefonts/fontbakery/issues/2179


</pre>

* ⚠ **WARN** The combined length of family and style exceeds 27 chars in the following 'WINDOWS' entries:
 FONT_FAMILY_NAME = 'Big Shoulders Inline Thin' / SUBFAMILY_NAME = 'Regular'

Please take a look at the conversation at https://github.com/googlefonts/fontbakery/issues/2179 in order to understand the reasoning behind these name table records max-length criteria. [code: too-long]

</details>
<details>
<summary>⚠ <b>WARN:</b> Checking unitsPerEm value is reasonable.</summary>

* [com.google.fonts/check/unitsperem](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/head.html#com.google.fonts/check/unitsperem)
<pre>--- Rationale ---

According to the OpenType spec:

The value of unitsPerEm at the head table must be a value between 16 and 16384.
Any value in this range is valid.

In fonts that have TrueType outlines, a power of 2 is recommended as this
allows performance optimizations in some rasterizers.

But 1000 is a commonly used value. And 2000 may become increasingly more common
on Variable Fonts.


</pre>

* ⚠ **WARN** In order to optimize performance on some legacy renderers, the value of unitsPerEm at the head table should idealy be a power of between 16 to 16384. And values of 1000 and 2000 are also common and may be just fine as well. But we got 4000 instead. [code: suboptimal]

</details>
<details>
<summary>⚠ <b>WARN:</b> The variable font 'opsz' (Optical Size) axis coordinate should be between 9 and 13 on the 'Regular' instance.</summary>

* [com.google.fonts/check/varfont/regular_opsz_coord](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/fvar.html#com.google.fonts/check/varfont/regular_opsz_coord)
<pre>--- Rationale ---

According to the Open-Type spec&#x27;s registered design-variation tag &#x27;opsz&#x27;
available at
https://docs.microsoft.com/en-gb/typography/opentype/spec/dvaraxistag_opsz

If a variable font has a &#x27;opsz&#x27; (Optical Size) axis, then the coordinate of its
&#x27;Regular&#x27; instance is recommended to be a value in the range 9 to 13.


</pre>

* ⚠ **WARN** The "opsz" (Optical Size) coordinate on the "Regular" instance is recommended to be a value in the range 9 to 13. Got 72.0 instead. [code: out-of-range]

</details>
<br>
</details>

### Summary

| 💔 ERROR | 🔥 FAIL | ⚠ WARN | 💤 SKIP | ℹ INFO | 🍞 PASS | 🔎 DEBUG |
|:-----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 0 | 2 | 5 | 87 | 8 | 93 | 0 |
| 0% | 1% | 3% | 45% | 4% | 48% | 0% |

**Note:** The following loglevels were omitted in this report:
* **SKIP**
* **INFO**
* **PASS**
* **DEBUG**