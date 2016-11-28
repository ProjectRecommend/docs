## Metrics

### Cyclomatic Complexity:

Cyclomatic Complexity corresponds to the number of decisions a block of code contains plus 1. This number (also called McCabe number) is equal to the number of linearly independent paths through the code. This number can be used as a guide when testing conditional logic in blocks.

#### Radon calculates CC in the following manner:

![CC Calculation Rubric](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/SoftwareCodingMetrices/CC.PNG)

### Raw Metrics:

The following are the definitions employed by Radon:

- LOC: The total number of lines of code. It does not necessarily correspond to the number of lines in the file.
- LLOC: The number of logical lines of code. Every logical line of code contains exactly one statement.
- SLOC: The number of source lines of code - not necessarily corresponding to the LLOC.
- Comments: The number of comment lines. Multi-line strings are not counted as comment since, to the Python interpreter, they are just strings.
- Multi: The number of lines which represent multi-line strings.
- Blanks: The number of blank lines (or whitespace-only once).

#### The equation SLOC - Single comments - Multi = LOC should always hold. Additionally, comment stats are calculated:

- C % L: the ratio between number of comment lines and LOC, expressed as a percentage;
- C % S: the ratio between number of comment lines and SLOC, expressed as a percentage;
- C + M % L: the ratio between number of comment and multiline strings lines and LOC, expressed as a percentage.

#### Halstead Metrics:
(important for calculation of Maintainability Index)

Halstead’s goal was to identify measurable properties of software, and the relations between them. These numbers are statically computed from the source code:

- η1 = the number of distinct operators
- η2 = the number of distinct operands
- N1 = the total number of operators
- N2 = the total number of operands

From these values several values are calculated:

- Program vocabulary: η=η1+η2
- Program length: N=N1+N2
- Calculated program length: Nˆ=η1log2η1+η2log2η2
- Volume: V=Nlog2η
- Difficulty: D=(n1/2)*(N2/n2)
- Effort: E=D⋅V
- Time required to program: T=E/18 seconds
- Number of delivered bugs: B=V/3000.

### Maintainability Index:

Maintainability Index is a software metric which measures how maintainable (easy to support and change) the source code is. The maintainability index is calculated as a factored formula consisting of SLOC (Source Lines Of Code), Cyclomatic Complexity and Halstead volume.

![MI Formula](https://raw.githubusercontent.com/ProjectRecommend/docs/master/design-docs/SoftwareCodingMetrices/MIFormula.PNG)

Where:
- V is the Halstead Volume (see below);
- G is the total Cyclomatic Complexity;
- L is the number of Source Lines of Code (SLOC);
- C is the percent of comment lines (important: converted to radians).
