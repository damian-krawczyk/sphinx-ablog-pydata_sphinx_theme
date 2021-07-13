# sphinx-ablog-pydata_sphinx_theme

1. `sphinx-quickstart docs`
    ```
    > Separate source and build directories (y/n) [n]:
    > Project name: Sphinx ablog pydata_sphinx_theme
    > Author name(s): Damian Krawczyk
    > Project release []: 0.0.1
    > Project language [en]: 
    ```
2. `cd docs`
3. `sphinx-build . _build`
4. `pip install ablog pydata_sphinx_theme`
5. `mkdir posts`
6. `cd posts`
7. `ablog post first-post`
    ```
    .. post:: Jul 13, 2021
       :tags: tag
       :author: Damian Krawczyk

    First Post
    ==========

    World, hello again!
    ```
8. `ablog post second-post`
    ```
    .. post:: Jul 13, 2021
       :tags: tag
       :author: Damian Krawczyk

    Second Post
    ===========

    World, hello again!
    ```
9. Add to `conf.py`:
    ```
    extensions = [
        'ablog',
        'sphinx.ext.intersphinx',
    ]
    html_theme = "pydata_sphinx_theme"
    ```
10. Add to main `index.rst`:
    ```
    Post list 
    =========

    .. postlist::
       :date: %d %B %Y
       :format: {date} - {title}
       :list-style: disk
    ```
11. `cd ..`
12. `sphinx-build . _build`