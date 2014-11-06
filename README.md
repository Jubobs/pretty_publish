pretty_publish

Author: Julien Cretel (jubobs.tex@gmail.com)

Improves LaTeX output of MATLAB's `publish` function by performing
syntax-highlighting of m-code

### Dependencies (compared to vanilla "publish")

 - `matlab-prettifier` LaTeX package (http://www.ctan.org/pkg/matlab-prettifier)

### Installation

 1. Install dependencies.
 2. Add the file `matlab2latex_pretty.xsl` to your search MATLAB path.
 3. Test that everything works well by running the following toy example

        publish('peaks',...
            struct('format','latex','stylesheet','matlab2latex_pretty.xsl'))

at the MATLAB command line.

### User guide

Specify `matlab2latex-pretty.xsl` as the stylesheet that `publish` should use:

    publish('<path-to-m-file>',...
        struct('format','latex','stylesheet','matlab2latex_pretty.xsl'))
