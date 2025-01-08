# Lua pairs iterator unexpected behavior

This repository demonstrates a potential issue with Lua's `pairs` iterator when modifying a table during iteration.  The code in `bug.lua` recursively iterates through a nested table.  However, if the table's structure is modified within the iteration (e.g., by adding or removing elements), the `pairs` iterator might not visit all elements as expected, leading to unexpected results.

The `bugSolution.lua` file offers a workaround to address this behavior.  It's important to note that modifying tables during iteration using `pairs` is generally discouraged due to the potential for unpredictable outcomes.  Consider alternative approaches, such as copying the table or using a different iteration method, to prevent such issues.