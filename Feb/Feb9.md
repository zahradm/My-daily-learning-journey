## What was the problem? How to solve it?

Adding more than one item to an existing Python set is as simple as creating an additional set, and then updating the old set. You can do this as follows:

`first_set = {'a', 'b', 'c'}`\
`second_set = {'e', 'f'}`\
`first_set.update(second_set)`
