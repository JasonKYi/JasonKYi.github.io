---
layout: page
title: "Lean in LaTeX with minted"
permalink: /lean-minted
---

<html lang='en-US' xml:lang='en-US'> 
<head><title>Lean in LaTeX with minted</title> 
<!-- <meta charset='utf-8' /> 
<meta content='TeX4ht (https://tug.org/tex4ht/)' name='generator' /> 
<meta content='width=device-width,initial-scale=1' name='viewport' /> 
<link href='main.css' rel='stylesheet' type='text/css' />  -->
</head><body>
<div class='maketitle'>                                                            

<h2 class='titleHead'>Lean in LaTeX with
<span id='textcolor1'><code class='minted-inline'>minted<!--  --></code></span></h2>
</div>
<!-- l. 37 --><p class='noindent'>In this short article I will describe how to include Lean snippets in your LaTeX document by using the
<code class='minted-inline'>minted<!--  --></code> package. The simplest
method is by including the <code class='minted-inline'>minted<!--  --></code>
package in your document via <code class='minted-inline'><span id='textcolor2'><strong>\usepackage</strong></span><span id='textcolor3'>{</span>minted<span id='textcolor4'>}</span><!--  --></code>
and include Lean code with
</p>
<pre class='fancyvrb' id='fancyvrb1'><a id='x1-11r1'></a><span id='textcolor5'><strong>\begin</strong></span><span id='textcolor6'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>minted</span><span id='textcolor7'><span class='ec-lmtt-10'>}{</span></span><span class='ec-lmtt-10'>lean</span><span id='textcolor8'><span class='ec-lmtt-10'>}</span></span> 
<a id='x1-13r2'></a><span class='ec-lmtt-10'>  &lt;code goes here&gt;</span> 
<a id='x1-15r3'></a><span id='textcolor9'><strong>\end</strong></span><span id='textcolor10'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>minted</span><span id='textcolor11'><span class='ec-lmtt-10'>}</span></span></pre>
<!-- l. 46 --><p class='noindent'>As an example, the following code
</p>
<pre class='fancyvrb' id='fancyvrb2'><a id='x1-24r1'></a><span id='textcolor12'><strong>\begin</strong></span><span id='textcolor13'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>minted</span><span id='textcolor14'><span class='ec-lmtt-10'>}{</span></span><span class='ec-lmtt-10'>lean</span><span id='textcolor15'><span class='ec-lmtt-10'>}</span></span> 
<a id='x1-26r2'></a><span class='ec-lmtt-10'>/-- **The second Borel-Cantelli lemma** -/</span> 
<a id='x1-28r3'></a><span class='ec-lmtt-10'>lemma measure</span><span id='textcolor16'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>limsup</span><span id='textcolor17'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>eq</span><span id='textcolor18'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>one </span><span id='textcolor19'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>s : ℕ → set </span><span id='textcolor20'><span class='ec-lmtt-10'>}</span></span> 
<a id='x1-30r4'></a><span class='ec-lmtt-10'>  (hsm : ∀ n, measurable</span><span id='textcolor21'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>set (s n)) (hs : Indep</span><span id='textcolor22'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>set s )</span> 
<a id='x1-32r5'></a><span class='ec-lmtt-10'>  (hs</span><span class='ts1-lmtt10-'>'</span><span class='ec-lmtt-10'> : ∑</span><span class='ts1-lmtt10-'>'</span><span class='ec-lmtt-10'> n,  (s n) = ∞) :</span> 
<a id='x1-34r6'></a><span class='ec-lmtt-10'>   (limsup s at</span><span id='textcolor23'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>top) = 1</span> 
<a id='x1-36r7'></a><span id='textcolor24'><strong>\end</strong></span><span id='textcolor25'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>minted</span><span id='textcolor26'><span class='ec-lmtt-10'>}</span></span></pre>
<!-- l. 57 --><p class='noindent'>will generate the following
</p>
<pre class='fancyvrb' id='fancyvrb3'><a id='x1-43r1'></a><span id='textcolor27'><i>/-- **The second Borel-Cantelli lemma** -/</i></span> 
<a id='x1-45r2'></a><span id='textcolor28'><strong>lemma</strong></span><span class='ec-lmtt-10'> measure_limsup_eq_one </span><span id='textcolor29'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>s </span><span id='textcolor30'><span class='ec-lmtt-10'>:</span></span><span class='ec-lmtt-10'> ℕ </span><span id='textcolor31'><span class='ec-lmtt-10'>→</span></span><span class='ec-lmtt-10'> set </span><span id='textcolor32'></span><span id='textcolor33'><span class='ec-lmtt-10'>}</span></span> 
<a id='x1-47r3'></a><span class='ec-lmtt-10'>  </span><span id='textcolor34'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>hsm </span><span id='textcolor35'><span class='ec-lmtt-10'>:</span></span><span class='ec-lmtt-10'> </span><span id='textcolor36'><span class='ec-lmtt-10'>∀</span></span><span class='ec-lmtt-10'> n</span><span id='textcolor37'><span class='ec-lmtt-10'>,</span></span><span class='ec-lmtt-10'> measurable_set </span><span id='textcolor38'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>s n</span><span id='textcolor39'><span class='ec-lmtt-10'>))</span></span><span class='ec-lmtt-10'> </span><span id='textcolor40'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>hs </span><span id='textcolor41'><span class='ec-lmtt-10'>:</span></span><span class='ec-lmtt-10'> Indep_set s </span><span id='textcolor42'><span class='ec-lmtt-10'>)</span></span> 
<a id='x1-49r4'></a><span class='ec-lmtt-10'>  </span><span id='textcolor43'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>hs</span><span class='ts1-lmtt10-'>'</span><span class='ec-lmtt-10'> </span><span id='textcolor44'><span class='ec-lmtt-10'>:</span></span><span class='ec-lmtt-10'> </span><span id='textcolor45'><span class='ec-lmtt-10'>∑</span><span class='ts1-lmtt10-'>'</span></span><span class='ec-lmtt-10'> n</span><span id='textcolor46'><span class='ec-lmtt-10'>,</span></span><span class='ec-lmtt-10'>  </span><span id='textcolor47'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>s n</span><span id='textcolor48'><span class='ec-lmtt-10'>)</span></span><span class='ec-lmtt-10'> </span><span id='textcolor49'><span class='ec-lmtt-10'>=</span></span><span class='ec-lmtt-10'> </span><span id='textcolor50'><span class='ec-lmtt-10'>∞</span></span><span id='textcolor51'><span class='ec-lmtt-10'>)</span></span><span class='ec-lmtt-10'> </span><span id='textcolor52'><span class='ec-lmtt-10'>:</span></span> 
<a id='x1-51r5'></a><span class='ec-lmtt-10'>   </span><span id='textcolor53'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>limsup s at_top</span><span id='textcolor54'><span class='ec-lmtt-10'>)</span></span><span class='ec-lmtt-10'> </span><span id='textcolor55'><span class='ec-lmtt-10'>=</span></span><span class='ec-lmtt-10'> </span><span id='textcolor56'><span class='ec-lmtt-10'>1</span></span></pre>
<!-- l. 66 --><p class='noindent'>You might encounter issues when displaying certain unicode resulting in a box
with a question mark in your file instead of a unicode. Namely, you might see a
<code class='minted-inline'><span id='textcolor57'>⨍</span><!--  --></code>
when your code snippet contains a unsupported unicode. To fix this, you can use the
<code class='minted-inline'>newunicodechar<!--  --></code>
package to introduce new unicode characters.
</p><!-- l. 71 --><p class='noindent'>For example, to display the following snippet correctly, we need to include the unicode characters
<code class='minted-inline'>ℒ<!--  --></code> and
<code class='minted-inline'><span id='textcolor58'>𝒩</span><!--  --></code>.
</p>
<pre class='fancyvrb' id='fancyvrb4'><a id='x1-63r1'></a><span id='textcolor59'><strong>\begin</strong></span><span id='textcolor60'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>minted</span><span id='textcolor61'><span class='ec-lmtt-10'>}{</span></span><span class='ec-lmtt-10'>lean</span><span id='textcolor62'><span class='ec-lmtt-10'>}</span></span> 
<a id='x1-65r2'></a><span class='ec-lmtt-10'>lemma unif</span><span id='textcolor63'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>integrable</span><span id='textcolor64'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>of</span><span id='textcolor65'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>tendsto</span><span id='textcolor66'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>Lp</span><span id='textcolor67'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>zero</span> 
<a id='x1-67r3'></a><span class='ec-lmtt-10'>  (hp : 1 ≤ p) (hp</span><span class='ts1-lmtt10-'>'</span><span class='ec-lmtt-10'> : p ≠ ∞) (hf : ∀ n, mem</span><span id='textcolor68'><span class='ec-lmtt-10'>_</span></span><span class='cmsy-10'>ℒ</span><span class='ec-lmtt-10'>p (f n) p )</span> 
<a id='x1-69r4'></a><span class='ec-lmtt-10'>  (hf</span><span id='textcolor69'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>tendsto : tendsto ( n, snorm (f n) p ) at</span><span id='textcolor70'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>top (</span><span class='cmsy-10'>𝒩</span><span class='ec-lmtt-10'> 0)) :</span> 
<a id='x1-71r5'></a><span class='ec-lmtt-10'>  unif</span><span id='textcolor71'><span class='ec-lmtt-10'>_</span></span><span class='ec-lmtt-10'>integrable f p </span> 
<a id='x1-73r6'></a><span id='textcolor72'><strong>\end</strong></span><span id='textcolor73'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>minted</span><span id='textcolor74'><span class='ec-lmtt-10'>}</span></span></pre>
                                                                            

                                                                            
<!-- l. 82 --><p class='noindent'>To achieve this, simply include the following code in your preamble.
</p>
<pre class='fancyvrb' id='fancyvrb5'><a id='x1-78r1'></a><span id='textcolor75'><strong>\usepackage</strong></span><span id='textcolor76'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>newunicodechar</span><span id='textcolor77'><span class='ec-lmtt-10'>}</span></span> 
<a id='x1-80r2'></a><span id='textcolor78'><strong>\newunicodechar</strong></span><span id='textcolor79'><span class='ec-lmtt-10'>{</span></span><span class='cmsy-10'>𝒩</span><span id='textcolor80'><span class='ec-lmtt-10'>}{</span></span><span id='textcolor81'><strong>\ensuremath</strong></span><span id='textcolor82'><span class='ec-lmtt-10'>{</span></span><span id='textcolor83'><strong>\mathcal</strong></span><span id='textcolor84'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>N</span><span id='textcolor85'><span class='ec-lmtt-10'>}}}</span></span> 
<a id='x1-82r3'></a><span id='textcolor86'><strong>\newunicodechar</strong></span><span id='textcolor87'><span class='ec-lmtt-10'>{</span></span><span class='cmsy-10'>ℒ</span><span id='textcolor88'><span class='ec-lmtt-10'>}{</span></span><span id='textcolor89'><strong>\ensuremath</strong></span><span id='textcolor90'><span class='ec-lmtt-10'>{</span></span><span id='textcolor91'><strong>\mathcal</strong></span><span id='textcolor92'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>L</span><span id='textcolor93'><span class='ec-lmtt-10'>}}}</span></span></pre>
<!-- l. 89 --><p class='noindent'>The above code then displays the following
</p>
<pre class='fancyvrb' id='fancyvrb6'><a id='x1-88r1'></a><span id='textcolor94'><strong>lemma</strong></span><span class='ec-lmtt-10'> unif_integrable_of_tendsto_Lp_zero</span> 
<a id='x1-90r2'></a><span class='ec-lmtt-10'>  </span><span id='textcolor95'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>hp </span><span id='textcolor96'><span class='ec-lmtt-10'>:</span></span><span class='ec-lmtt-10'> </span><span id='textcolor97'><span class='ec-lmtt-10'>1</span></span><span class='ec-lmtt-10'> </span><span id='textcolor98'><span class='ec-lmtt-10'>≤</span></span><span class='ec-lmtt-10'> p</span><span id='textcolor99'><span class='ec-lmtt-10'>)</span></span><span class='ec-lmtt-10'> </span><span id='textcolor100'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>hp</span><span class='ts1-lmtt10-'>'</span><span class='ec-lmtt-10'> </span><span id='textcolor101'><span class='ec-lmtt-10'>:</span></span><span class='ec-lmtt-10'> p </span><span id='textcolor102'><span class='ec-lmtt-10'>≠</span></span><span class='ec-lmtt-10'> </span><span id='textcolor103'><span class='ec-lmtt-10'>∞</span></span><span id='textcolor104'><span class='ec-lmtt-10'>)</span></span><span class='ec-lmtt-10'> </span><span id='textcolor105'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>hf </span><span id='textcolor106'><span class='ec-lmtt-10'>:</span></span><span class='ec-lmtt-10'> </span><span id='textcolor107'><span class='ec-lmtt-10'>∀</span></span><span class='ec-lmtt-10'> n</span><span id='textcolor108'><span class='ec-lmtt-10'>,</span></span><span class='ec-lmtt-10'> mem_</span><span class='cmsy-10'>ℒ</span><span class='ec-lmtt-10'>p </span><span id='textcolor109'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>f n</span><span id='textcolor110'><span class='ec-lmtt-10'>)</span></span><span class='ec-lmtt-10'> p </span><span id='textcolor111'><span class='ec-lmtt-10'>)</span></span> 
<a id='x1-92r3'></a><span class='ec-lmtt-10'>  </span><span id='textcolor112'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>hf_tendsto </span><span id='textcolor113'><span class='ec-lmtt-10'>:</span></span><span class='ec-lmtt-10'> tendsto </span><span id='textcolor114'><span class='ec-lmtt-10'>(</span></span><span id='textcolor115'></span><span class='ec-lmtt-10'> n</span><span id='textcolor116'><span class='ec-lmtt-10'>,</span></span><span class='ec-lmtt-10'> snorm </span><span id='textcolor117'><span class='ec-lmtt-10'>(</span></span><span class='ec-lmtt-10'>f n</span><span id='textcolor118'><span class='ec-lmtt-10'>)</span></span><span class='ec-lmtt-10'> p </span><span id='textcolor119'><span class='ec-lmtt-10'>)</span></span><span class='ec-lmtt-10'> at_top </span><span id='textcolor120'><span class='ec-lmtt-10'>(</span></span><span id='textcolor121'><span class='cmsy-10'>𝒩</span></span><span class='ec-lmtt-10'> </span><span id='textcolor122'><span class='ec-lmtt-10'>0</span></span><span id='textcolor123'><span class='ec-lmtt-10'>))</span></span><span class='ec-lmtt-10'> </span><span id='textcolor124'><span class='ec-lmtt-10'>:</span></span> 
<a id='x1-94r4'></a><span class='ec-lmtt-10'>  unif_integrable f p </span></pre>
<!-- l. 96 --><p class='noindent'>Hence, whenever you encounter a unsupported unicode, simply introduce it with by
finding a symbol in math mode which which is similar enough to that unicode and
declaring
</p>
<pre class='fancyvrb' id='fancyvrb7'><a id='x1-97r1'></a><span id='textcolor125'><strong>\newunicodechar</strong></span><span id='textcolor126'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>&lt;unicode&gt;</span><span id='textcolor127'><span class='ec-lmtt-10'>}{</span></span><span id='textcolor128'><strong>\ensuremath</strong></span><span id='textcolor129'><span class='ec-lmtt-10'>{</span></span><span class='ec-lmtt-10'>&lt;math replacement&gt;</span><span id='textcolor130'><span class='ec-lmtt-10'>}}</span></span></pre>
<!-- l. 103 --><p class='noindent'>Beyond this, you can also customize the style the code snippet is displayed using options available
in <code class='minted-inline'>minted<!--  --></code>. See
this <a href='https://www.overleaf.com/learn/latex/Code_Highlighting_with_minted'>Overleaf article</a> or the <a href='https://tug.ctan.org/macros/latex/contrib/minted/minted.pdf'>official documentation</a> for more details.
</p>
 
</body> 
</html>