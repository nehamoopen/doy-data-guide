# Naming Conventions

## What Is A Naming Convention?

A naming convention is a set of rules for naming things. You can apply it to things like folders, files, and variables.

## Why Should I Apply A Naming Convention?

Names that are informative and useful for machines and humans are a step toward efficient data management and reproducible research. The more consistent and meaningful the name, the easier it will be to locate and identify things, understand what they contain, and (re)use them.

## When Should I Apply A Naming Convention?

Aim to select and implement a naming convention at the beginning of a project. If you want to retroactively apply a naming convention, there are several tools for bulk renaming.

The entire research team should agree on and adopt a naming convention. Document the choice of naming convention in the DMP, so others can refer to and grasp it quickly.

![](images/xkcd-file-naming.png)

<figcaption><a href="https://xkcd.com/1459/">Documents - xkcd</a>. Used under a CC BY-NC 2.5 license. </figcaption>

## Popular Naming Conventions

Instead of developing a naming convention from scratch, you can start with one that is already being used in programming and software development communities:

| Naming Covention | Example           | Description |
| ---------------- | ----------------- | ----------- |
| original name    | `an awesome name` | N/A
| snake_case       | `an_awesome_name` | All words are lowercase and separated by an underscore ( `_` ) |
| kebab-case       | `an-awesome-name` | All words are lowercase and separated by a hyphen ( `-` ) |
| PascalCase       | `AnAwesomeName`   | All words are capitalized. Spaces are not used. |
| camelCase        | `anAwesomeName`   | The first word is lowercase, the remaining words are capitalized. Spaces are not used. |

## Human-Readable Names

You can tailor naming conventions like `snake_case` and `PascalCase` to suit your project and workflow. Determine what information is relevant (or not) to create meaningful names and how you can string this information together. Don't forget to document this in your DMP!

!!! note "Elements for Human-Readable Names"

    Names should be =<25 characters long and can include:

    - Date of creation/update (`YYYY-MM-DD` or `YYYYMMDD`)
    - Description of content, like type of data
    - Initials of creator/reviewer
    - Project number or acronym
    - Location/coordinates
    - Version number (like `v2` or v2.2`)

## Machine-Readable Names

When names are machine-readable, they can be efficiently processed by computers and software. This makes it easier to search for files and run operations that involve programming like extracting information from file names or working with regular expressions.  

!!! note "Avoid"

    - Spaces
    - Special characters like `$`, `@`, `%`, `#`, `&`, `*`, `!`, `/`, `\`
    - Punction characters like `,`, `:`, `;`, `?`, `'`, `"`
    - Accented characters

## A Note on Numbering, Dates, Versioning

- Append numbers to the beginning of a name to enable sorting according to a logical structure. Use multiple digits like `01` or `001`.

- Dates should follow the ISO 8601 standard which is either `YYYY-MM-DD` or `YYYYMMDD`. Append dates to the beginning of names to enable sorting in chronological order.

- Specify versions using ordinal numbers (1,2,3) for major revisions and decimals for minor changes (1.1, 1.2, 2.1, 2.2). Alternatively, you can specify versions with multiple digits like v01 and v02.

## Renaming files

The following tools enable renaming in bulk:

- [Bulk Rename Utility](https://www.bulkrenameutility.co.uk/) (Windows, free)
- [Renamer](https://renamer.com/) (MacOS, paid)
- [NameChanger](https://mrrsoftware.com/namechanger/), (MacOS, free)
- [GPRename](https://gprename.sourceforge.net/) (Linux, free)

## References

1. [https://en.wikipedia.org/wiki/Naming_convention](https://en.wikipedia.org/wiki/Naming_convention)
2. [https://help.osf.io/article/146-file-naming](https://help.osf.io/article/146-file-naming)
3. [https://rdm.elixir-belgium.org/file_naming.html](https://rdm.elixir-belgium.org/file_naming.html)
4. [https://khalilstemmler.com/blogs/camel-case-snake-case-pascal-case/](https://khalilstemmler.com/blogs/camel-case-snake-case-pascal-case/)
5. [https://dev.to/chaseadamsio/most-common-programming-case-types-30h9](https://dev.to/chaseadamsio/most-common-programming-case-types-30h9)
6. [https://rdmkit.elixir-europe.org/data_organisation](https://rdmkit.elixir-europe.org/data_organisation)
[http://dataabinitio.com/?p=987](http://dataabinitio.com/?p=987)
7. [https://dmeg.cessda.eu/Data-Management-Expert-Guide/2.-Organise-Document/File-naming-and-folder-structure](https://dmeg.cessda.eu/Data-Management-Expert-Guide/2.-Organise-Document/File-naming-and-folder-structure)
8. [https://annakrystalli.me/rrresearchACCE20/filenaming-view.html](https://annakrystalli.me/rrresearchACCE20/filenaming-view.html)
