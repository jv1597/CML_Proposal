# CML_Proposal
Content Markup Language
I'm proposing a new markup language script referred to as Content Markup Language (CML).

Content Markup Language (CML)

Port Tag:
Syntax:  <port [port], [seq=0/1], [input=0/1], [attributes], [coord]>'+'

Source Tag:
Syntax:  <source [href](+)[line], [seq=0/1], [input=0/1], [css_href=0/1], [attributes], [coord]>'+'

Destination Tag:
Syntax:  <destination [href](+)[line], [seq=0/1], [input=0/1], [css_href=0/1], [attributes], [coord]>

CSS Tag:
Syntax:  <css>/</css>

Appendation Operator:Syntax:
Internal Append Script:  (+)  (placed after href patch specificaiton for specific sequence retrieval)
External Append Script:   +  (placed at the end of either <port>, or <source> tags for appending of source code)

CSS is accomplished by specifying css_href, on or off, and appending singular/multiple source records to a singular
destination record for retrieval, and appliance of style attributes to page objects as in the following code:

**CSS Batch**
<source [href](+)[line], [seq=0/1], [input=0/1], [css_href=0/1], [attributes], [coord]>+
<source [href](+)[line], [seq=0/1], [input=0/1], [css_href=0/1], [attributes], [coord]>+
<source [href](+)[line], [seq=0/1], [input=0/1], [css_href=0/1], [attributes], [coord]>+
<destination [css_record.html]>

CSS batch sources must be grouped in the preferred sequential order.  The <css> tag encapsulates the source batch for css
attribution on the sources in sequential order from the css record, being css_record.html, for this example.

**CSS Attribution**
<css href='path/css_record.html'>
<source [href](+)[line], [seq=0/1], [input=0/1], [css_href=0/1], [attributes], [coord]>
<source [href](+)[line], [seq=0/1], [input=0/1], [css_href=0/1], [attributes], [coord]>
<source [href](+)[line], [seq=0/1], [input=0/1], [css_href=0/1], [attributes], [coord]>
</css>

The <port> tag enables portability with real-time data ports, encryption/decryption, and porting to window popups, window tabs,
and viewport for full screen applications.

The internal '(+)' tag operator enables html sequence tag parsing within html records, for access to specific html lines of
source code.  The (+) tag operator retreives specific line text, and the (+r) tag operator runs specific lines of html source
code.

Sequence html code is as simple as <1></1>, <2></2>, etc..  Runtime clipboard sequencing, like for chat applications that don't
require any permanent data storage, can be accomplished by overwriting the clipboard record with runtime sequences, and retreiving
at specified read intervals.

Forms are created with one main form image source, and multiple text sources as for example:

**Forms
<source href='path/form_backdrop_image.jpg', 0, 0, null, [coord]>

<source text='This is the Name field', [coord]>
<source text='This is the Address field', [coord]>
<source text='This is the City, and State field', [coord]>

<source href='path/field_batch.html>

The fields are called up by the field_batch source code to be rendered at their corresponding coordinates.

Form, and CSS source coding is coded sequentially for applicatiance of attributes, and storage sequencing.  All other page object
source code can be coded in any order.  All page objects are stored within the same folder belonging to the page, for more efficient
coding, and root access throughput.

Let me know what you think.
Jacob
