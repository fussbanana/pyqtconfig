---
description: AI rules derived by SpecStory from the project AI interaction history
globs: *
---

## HEADERS

## PROJECT RULES

## CODING STANDARDS

## WORKFLOW & RELEASE RULES

## TECH STACK

## DEBUGGING

- **Type Errors with `dict_keys`:** When encountering type errors related to using `dict_keys` where a `Sequence[str]` is expected (e.g., in the `addItems` method of `QComboBox`), explicitly convert the `dict_keys` object to a list using `list(map_dict.keys())`. This ensures that a proper sequence is passed to the method.
    - **Alternative:** If necessary, convert the keys to strings using a list comprehension: `[str(key) for key in map_dict.keys()]`.
    - **Alternative:** Iterate explicitly through the keys and add them one by one:
    ```python
    for key in map_dict.keys():
        cmb.addItem(key)
    ```
    - **Recommendation:** The `list(map_dict.keys())` approach is generally preferred for its readability and performance.

## PROJECT DOCUMENTATION & CONTEXT SYSTEM

## BEST PRACTICES