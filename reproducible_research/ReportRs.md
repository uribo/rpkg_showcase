

# ReporteRs: Microsoft Word, Microsoft Powerpoint and HTML Documents Generation

Microsoft関係のドキュメントを生成

[![](http://www.r-pkg.org/badges/version/ReporteRs)](http://cran.rstudio.com/web/packages/ReporteRs/index.html)

* CRAN: http://cran.r-project.org/web/packages/ReporteRs/index.html
* GitHub: https://github.com/davidgohel/ReporteRs
* URL: http://davidgohel.github.io/ReporteRs/index.html, http://groups.google.com/group/reporters-package


```r
> library(ReporteRs)
```

```
Loading required package: ReporteRsjars
```

バージョン: 0.8.2

-----



| 関数名 | 概略 |
|--------|------|
| `+.pot` | pot concatenation |
| `BootstrapMenu` | Create a bootstrap DropDownMenu |
| `CodeBlock` | Code Block Object |
| `DropDownMenu` | Create a bootstrap DropDownMenu |
| `FlexCell` | Cell object for FlexTable |
| `FlexRow` | Row object for FlexTable |
| `FlexTable` | FlexTable creation |
| `FontMetric` | Font metric |
| `Footnote` | Create a Footnote |
| `RScript` | RScript object |
| `ReporteRs-package` | ReporteRs: a package to create document from R |
| `[<-.FlexRow` | modify FlexRow content |
| `[<-.FlexTable` | alter FlexTable content and format |
| `add.plot.interactivity` | add interactivity on a plot |
| `add.pot` | add a paraggraph to an existing set of paragraphs of text |
| `addBootstrapMenu` | add a 'BootstrapMenu' into a 'bsdoc' object. |
| `addCodeBlock` | Add code block into a document object |
| `addCodeBlock.bsdoc` | Add a code block into a bsdoc object |
| `addCodeBlock.docx` | Add a code block into a docx object |
| `addCodeBlock.pptx` | Add a code block into a pptx object |
| `addColumnBreak` | Add a column break into a section |
| `addColumnBreak.docx` | Insert a column break into a docx section |
| `addDate` | Insert a date into a document object |
| `addDate.pptx` | Insert a date shape into a document pptx object |
| `addDocument` | Add an external document into a document object |
| `addDocument.docx` | Add external document into a docx object |
| `addFlexTable` | Insert a FlexTable into a document object |
| `addFlexTable.bsdoc` | Insert a FlexTable into an bsdoc object |
| `addFlexTable.docx` | Insert a FlexTable into a docx object |
| `addFlexTable.pptx` | Insert a FlexTable into a pptx object |
| `addFooter` | Insert a footer into a document object |
| `addFooter.bsdoc` | Add text in footer of a 'bsdoc' object |
| `addFooter.pptx` | Insert a footer shape into a document pptx object |
| `addFooterRow` | add footer in a FlexTable |
| `addHeaderRow` | add header in a FlexTable |
| `addIframe` | Add an iframe into a document object |
| `addIframe.bsdoc` | Insert an iframe into a bsdoc object |
| `addImage` | Add an external image into a document object |
| `addImage.bsdoc` | Insert an external image into a bsdoc object |
| `addImage.docx` | Add external image into a docx object |
| `addImage.pptx` | Insert an external image into a pptx object |
| `addJavascript` | add javascript into a bsdoc object |
| `addLinkItem` | add an item in a 'BootstrapMenu' or a 'DropDownMenu' |
| `addMarkdown` | Add a markdown text or file |
| `addMarkdown.bsdoc` | Add a markdown text or file into an bsdoc object |
| `addMarkdown.docx` | Add a markdown text or file into a docx object |
| `addMarkdown.pptx` | Add a markdown text or file into a pptx object |
| `addPageBreak` | Add a page break into a document object |
| `addPageBreak.docx` | Insert a page break into a docx object |
| `addPageNumber` | Insert a page number into a document object |
| `addPageNumber.pptx` | Insert a page number shape into a document pptx object |
| `addParagraph` | Add a paragraph into a document object |
| `addParagraph.Footnote` | Insert a paragraph into a Footnote object |
| `addParagraph.bsdoc` | Insert a paragraph into an bsdoc object |
| `addParagraph.docx` | Insert a paragraph into a docx object |
| `addParagraph.pptx` | Insert a paragraph into a pptx object |
| `addPlot` | Add a plot into a document object |
| `addPlot.bsdoc` | Add a plot into an bsdoc object |
| `addPlot.docx` | Add a plot into a docx object |
| `addPlot.pptx` | Add a plot into a pptx object |
| `addPostCommand` | add post plot commands |
| `addRScript` | Add R script into a document object |
| `addRScript.bsdoc` | Add R script into a bsdoc object |
| `addRScript.docx` | Add R script into a docx object |
| `addRScript.pptx` | Add R script into a pptx object |
| `addSection` | Add a section into a document object |
| `addSection.docx` | Add a section into a docx object |
| `addSlide` | Add a slide into a document object |
| `addSlide.pptx` | Insert a slide into a pptx object |
| `addSubtitle` | Add a subtitle shape into a document object |
| `addSubtitle.pptx` | Insert a addSubtitle shape into a pptx object |
| `addTOC` | Add a table of contents into a document object |
| `addTOC.bsdoc` | Insert a table of contents into a bsdoc object |
| `addTOC.docx` | Insert a table of contents into a docx object |
| `addTitle` | Add a title into a document object |
| `addTitle.bsdoc` | Insert a title into a bsdoc object |
| `addTitle.docx` | Insert a title into a docx object |
| `addTitle.pptx` | Insert a title into a pptx object |
| `as.FlexTable` | R tables as FlexTables |
| `as.FlexTable.sessionInfo` | get FlexTable from a sessionInfo object |
| `as.html` | get HTML code |
| `as.html.FlexTable` | get HTML code from a FlexTable |
| `as.html.RScript` | get HTML code from a RScript object |
| `as.html.bsdoc` | get HTML code from a bsdoc object |
| `as.html.pot` | get HTML code from a pot |
| `borderDashed` | shortcut for dashed border |
| `borderDotted` | shortcut for dotted border |
| `borderNone` | shortcut for no border |
| `borderProperties` | border properties object |
| `borderSolid` | shortcut for solid border |
| `bsdoc` | Create an object representation of a bootstrap html document |
| `cellProperties` | Cell formatting properties |
| `chprop` | Change a formatting properties object |
| `chprop.borderProperties` | Modify border formatting properties |
| `chprop.cellProperties` | Modify a cell formatting properties object |
| `chprop.parProperties` | Modify paragraph formatting properties |
| `chprop.textProperties` | Modify text formatting properties |
| `declareTitlesStyles` | Set manually headers'styles of a document object |
| `declareTitlesStyles.docx` | Set manually headers'styles of a docx object |
| `deleteBookmark` | delete a bookmark into a docx object |
| `deleteBookmarkNextContent` | delete first content after a bookmark into a docx object |
| `dim.docx` | Get page layout dimensions of a Word document |
| `dim.pptx` | Get layout information on a PowerPoint slide |
| `doc-list-settings` | format ordered and unordered lists |
| `docx` | Create Microsoft Word document object representation |
| `docx-bookmark` | docx bookmarks |
| `is.color` | color checking |
| `light.table` | get a simple FlexTable from a dataset |
| `list_bookmarks` | List Bookmarks from a Word Document |
| `parCenter` | shortcut for centered alignment |
| `parJustify` | shortcut for justified alignment |
| `parLeft` | shortcut for left alignment |
| `parProperties` | Paragraph formatting properties |
| `parRight` | shortcut for right alignment |
| `pot` | Piece of Text (formated text) |
| `pot_img` | Image to be concatenate with pot object |
| `pptx` | Create Microsoft PowerPoint document object representation |
| `print.FlexTable` | Print FlexTables |
| `print.Footnote` | print a Footnote |
| `print.bsdoc` | Print method for 'bsdoc' objects. |
| `print.docx` | print informations about an object of class 'docx'. |
| `print.pot` | Print pot objects |
| `print.pptx` | print informations about an object of class 'pptx'. |
| `print.textProperties` | print formatting properties |
| `raphael.html` | get HTML code from a plot |
| `raphael_clicks` | clicks instructions to raphael device |
| `raphael_dbclicks` | tooltips instructions to raphael device |
| `raphael_tooltips` | tooltips instructions to raphael device |
| `raphael_tracer_off` | trace id off signal |
| `raphael_tracer_on` | trace id on signal |
| `registerRaphaelGraph` | register Raphael plots |
| `reporters_str_width` | Compute the width of a string |
| `setColumnsColors` | applies background colors to columns of a FlexTable |
| `setFlexTableBackgroundColors` | applies background colors to cells of a FlexTable |
| `setFlexTableBorders` | change grid lines of a FlexTable |
| `setFlexTableWidths` | set columns widths of a FlexTable |
| `setRowsColors` | applies background colors to rows of a FlexTable |
| `setZebraStyle` | FlexTable rows zebra striping |
| `set_of_paragraphs` | Set of paragraphs of text |
| `slide.layouts` | Get layout names of a document object |
| `slide.layouts.pptx` | Get layout names of a pptx document |
| `spanFlexTableColumns` | Span columns within rows |
| `spanFlexTableRows` | Span rows within columns |
| `styles` | Get styles names of a document object |
| `styles.docx` | Get styles names of a docx document |
| `textBold` | shortcut for bold |
| `textBoldItalic` | shortcut for bold italic |
| `textItalic` | shortcut for italic |
| `textNormal` | shortcut for default textProperties |
| `textProperties` | Text formatting properties |
| `text_extract` | Simple Text Extraction From a Word Document |
| `toc.options` | Set TOC options for a document object |
| `toc.options.docx` | Set TOC options |
| `triggerPostCommand` | trigger post plot commands |
| `vanilla.table` | get a simple FlexTable from a dataset |
| `writeDoc` | Write a document object |
| `writeDoc.bsdoc` | Write a 'bsdoc' object in a html file |
| `writeDoc.docx` | Write a docx object in a docx file |
| `writeDoc.pptx` | Write a pptx object in a pptx file |

-----
