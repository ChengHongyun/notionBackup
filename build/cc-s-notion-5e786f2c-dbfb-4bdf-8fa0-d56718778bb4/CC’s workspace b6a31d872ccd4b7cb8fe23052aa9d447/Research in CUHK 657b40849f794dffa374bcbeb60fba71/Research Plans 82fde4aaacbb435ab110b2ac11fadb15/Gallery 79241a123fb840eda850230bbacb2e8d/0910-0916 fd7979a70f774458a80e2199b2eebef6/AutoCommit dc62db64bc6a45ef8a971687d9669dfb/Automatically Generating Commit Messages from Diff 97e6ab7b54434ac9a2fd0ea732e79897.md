# Automatically Generating Commit Messages from Diffs using Neural Machine Translation

Defect: Generally speaking, future improvements are likely to lie in targeted training for certain types of commits, combined with detection of change types. It is probable that very high quality predictions are possible for some types of software changes, but not others. This work provides a foundation for those and other future developments.
Github Repo: https://sjiang1.github.io/commitgen
Input: a corpus of diffs
and human-written commit messages from the top 1k Github
projects
Output: Our evaluation
uncovered a pattern in which the messages we generate tend to
be either very high or very low quality. Therefore, we created a
quality-assurance filter to detect cases in which we are unable to
produce good messages, and return a warning instead.


Venue: ASE
Years: 2017