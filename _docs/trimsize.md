---
title: Trim Sizes
---
<!-- trimsize -->
<!-- ### Trimsize -->

Due to the range of physical book form factors, the PDF compilation includes a `trimzize` option. The Word document has a fixed trim size (Letter, 1″ margins) to support editor collaboration. The ePUB and HTML lack trim sizes.

When calculating trim size, we filtered commonly used against those offered by [KDP][KDP]. The resulting set of trim sizes are listed below. Metric measures rounded to 2 digits in the table. All measures are in metric in the LaTeX macros. Since [Customary Measures][measure] are defined by their Metric equivalent, the PDF trim size is defined in metric.

[KDP]: https://kdp.amazon.com/en_US#trim
[measure]: https://en.wikipedia.org/wiki/United_States_customary_units#:~:text=For%20measuring%20length%2C%20the%20U.S.,for%20some%20applications%20in%20surveying.

<table class='text-center'>
<thead>
  <tr>
  <th>Trim Size</th>
  <th>Setting</th>
  <th>Region</th>
  <th colspan='2'>Paper Size</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Novella</td>
    <td><code>Novella</code></td>
    <td>US</td>
    <td>5″&nbsp;×&nbsp;8″</td>
    <td>12.7&nbsp;×&nbsp;20.32&nbsp;cm</td>
  </tr>
  <tr class='uk'>
    <td>UK B Format</td>
    <td><code>B-Format</code></td>
    <td>UK</td>
    <td>5.06″&nbsp;×&nbsp;7.81″</td>
    <td>12.85&nbsp;×&nbsp;19.84&nbsp;cm</td>
  </tr>
  <tr>
    <td>Small Trade</td>
    <td><code>SmallTrade</code></td>
    <td>US</td>
    <td>5.25″&nbsp;×&nbsp;8″</td>
    <td>13.34&nbsp;×&nbsp;20.32&nbsp;cm</td>
  </tr>
  <tr>
    <td>Digest</td>
    <td><code>Digest</code></td>
    <td>US</td>
    <td>5.5″&nbsp;×&nbsp;8.5″</td>
    <td>13.97&nbsp;×&nbsp;21.59&nbsp;cm</td>
  </tr>
  <tr>
    <td>Trade</td>
    <td><code>Trade</code></td>
    <td>US</td>
    <td>6″&nbsp;×&nbsp;9″</td>
    <td>15.24&nbsp;×&nbsp;22.86&nbsp;cm</td>
  </tr>
  <tr class='uk'>
    <td>Royal</td>
    <td><code>Royal</code></td>
    <td>UK</td>
    <td>6.14″&nbsp;×&nbsp;9.21″</td>
    <td>15.6&nbsp;×&nbsp;23.39&nbsp;cm</td>
  </tr>
  <tr>
    <td>Textbook</td>
    <td><code>Textbook</code></td>
    <td>US</td>
    <td>7″&nbsp;×&nbsp;10″</td>
    <td>17.78&nbsp;×&nbsp;25.4&nbsp;cm</td>
  </tr>
  <tr class='uk'>
    <td>Crown</td>
    <td><code>Crown</code></td>
    <td>UK</td>
    <td>7.44″&nbsp;×&nbsp;9.69″</td>
    <td>18.9&nbsp;×&nbsp;24.61&nbsp;cm</td>
  </tr>
  <tr>
    <td>Large Trade</td>
    <td><code>LargeTrade</code></td>
    <td>US</td>
    <td>8″&nbsp;×&nbsp;10″</td>
    <td>20.32&nbsp;×&nbsp;25.4&nbsp;cm</td>
  </tr>
  <tr>
    <td>Square</td>
    <td><code>Square</code></td>
    <td>US</td>
    <td>8.5″&nbsp;×&nbsp;8.5″</td>
    <td>21.59&nbsp;×&nbsp;21.59&nbsp;cm</td>
  </tr>
  <tr>
    <td>Letter</td>
    <td><code>Letter</code></td>
    <td>US</td>
    <td>8.5″&nbsp;×&nbsp;11″</td>
    <td>21.59&nbsp;×&nbsp;27.94&nbsp;cm</td>
  </tr>
  <tr class='uk'>
    <td>A4</td>
    <td><code>A4</code></td>
    <td>UK</td>
    <td>8.27″&nbsp;×&nbsp;11.69″</td>
    <td>21&nbsp;×&nbsp;29.7&nbsp;cm</td>
  </tr>
</tbody>
</table>
<!-- |    | 6.69"&nbsp;×&nbsp;9.61"         | 16.99&nbsp;×&nbsp;24.41&nbsp;cm | -->
<!-- |    | 7.5"&nbsp;×&nbsp;9.25"          | 19.05&nbsp;×&nbsp;23.5&nbsp;cm | -->
<!-- |    | 8.25"&nbsp;×&nbsp;6"          | 20.96&nbsp;×&nbsp;15.24&nbsp;cm | -->
<!-- |    | 8.25"&nbsp;×&nbsp;8.25"         | 20.96&nbsp;×&nbsp;20.96&nbsp;cm | -->

* Top and Inner margins are 2cm (~3/4″).
* Outer and bottom margins are 17mm (~5/8″).
* Gutter margin is added to the Inner margin based on estimated page count. This complies with KDP's standard.
* When attribute `bleed: true` is set, then the paper size and margins are increased by 3mm wide and 6mm high. (I don't think we can bleed an image, though.)
* Set attribute `crop: true` to see what a given size looks like scaled properly on a letter-sized printout.

**Warning:** Failure to use one of the listed trim sizes will cause the compilation to fail. Defaults to `trimsize: Trade`.
<!-- /trimsize -->
