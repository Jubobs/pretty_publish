# pretty_publish

Author: Julien Cretel (jubobs.tex@gmail.com)

Improves LaTeX output of MATLAB's `publish` function by performing
syntax-highlighting of m-code. The `-toc` file also enables multi-level
headers and a table of contents at the beginning.

## Dependencies (compared to vanilla "publish")

 - `matlab-prettifier` LaTeX package (http://www.ctan.org/pkg/matlab-prettifier)

## Installation

 1. Install dependencies.
 2. Add the file `matlab2latex_pretty.xsl` to your search MATLAB path.
 3. Test that everything works well by running the following toy example

        publish('peaks',...
            struct('format','latex','stylesheet','matlab2latex_pretty.xsl'))

at the MATLAB command line.

## User guide

### Without header numbering and TOC
Specify `matlab2latex-pretty.xsl` as the stylesheet that `publish` should use:

    publish('<path-to-m-file>',...
        struct('format','latex','stylesheet','matlab2latex_pretty.xsl'))

### With header numbering and TOC
If you want multi-level numbered headers, edit your MATLAB section headers such that they start
with underscores `_`, depending on the desired level.

For a top level section use:

    %% This is a top level section
    % With a short description
    
For a subsection use:

    %% _This will be a subsection
    % With a short description
    
For a subsubsection use:

    %% __This will be a subsubsection
    % With a short description

Specify `matlab2latex-pretty-toc.xsl` as the stylesheet that `publish` should use:

    publish('<path-to-m-file>',...
            struct('format','latex','stylesheet','matlab2latex_pretty.xsl'))
