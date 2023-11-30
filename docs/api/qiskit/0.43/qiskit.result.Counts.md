---
title: Counts
description: API reference for qiskit.result.Counts
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.result.Counts
---

# Counts

<span id="qiskit.result.Counts" />

`Counts(data, time_taken=None, creg_sizes=None, memory_slots=None)`

Bases: `dict`

A class to store a counts result from a circuit execution.

Build a counts object

**Parameters**

*   **data** (*dict*) –

    The dictionary input for the counts. Where the keys represent a measured classical value and the value is an integer the number of shots with that result. The keys can be one of several formats:

    > *   A hexadecimal string of the form `'0x4a'`
    > *   A bit string prefixed with `0b` for example `'0b1011'`
    > *   A bit string formatted across register and memory slots. For example, `'00 10'`.
    > *   A dit string, for example `'02'`. Note for objects created with dit strings the `creg_sizes` and `memory_slots` kwargs don’t work and [`hex_outcomes()`](qiskit.result.Counts#hex_outcomes "qiskit.result.Counts.hex_outcomes") and [`int_outcomes()`](qiskit.result.Counts#int_outcomes "qiskit.result.Counts.int_outcomes") also do not work.

*   **time\_taken** (*float*) – The duration of the experiment that generated the counts in seconds.

*   **creg\_sizes** (*list*) – a nested list where the inner element is a list of tuples containing both the classical register name and classical register size. For example, `[('c_reg', 2), ('my_creg', 4)]`.

*   **memory\_slots** (*int*) – The number of total `memory_slots` in the experiment.

**Raises**

*   **TypeError** – If the input key type is not an `int` or `str`.
*   **QiskitError** – If a dit string key is input with `creg_sizes` and/or `memory_slots`.

## Methods

<span id="qiskit-result-counts-clear" />

### clear

<span id="qiskit.result.Counts.clear" />

`Counts.clear() → None.  Remove all items from D.`

<span id="qiskit-result-counts-copy" />

### copy

<span id="qiskit.result.Counts.copy" />

`Counts.copy() → a shallow copy of D`

<span id="qiskit-result-counts-fromkeys" />

### fromkeys

<span id="qiskit.result.Counts.fromkeys" />

`Counts.fromkeys(value=None, /)`

Create a new dictionary with keys from iterable and values set to value.

<span id="qiskit-result-counts-get" />

### get

<span id="qiskit.result.Counts.get" />

`Counts.get(key, default=None, /)`

Return the value for key if key is in the dictionary, else default.

<span id="qiskit-result-counts-hex-outcomes" />

### hex\_outcomes

<span id="qiskit.result.Counts.hex_outcomes" />

`Counts.hex_outcomes()`

Return a counts dictionary with hexadecimal string keys

**Returns**

**A dictionary with the keys as hexadecimal strings instead of**

bitstrings

**Return type**

dict

**Raises**

**QiskitError** – If the Counts object contains counts for dit strings

<span id="qiskit-result-counts-int-outcomes" />

### int\_outcomes

<span id="qiskit.result.Counts.int_outcomes" />

`Counts.int_outcomes()`

Build a counts dictionary with integer keys instead of count strings

**Returns**

A dictionary with the keys as integers instead of bitstrings

**Return type**

dict

**Raises**

**QiskitError** – If the Counts object contains counts for dit strings

<span id="qiskit-result-counts-items" />

### items

<span id="qiskit.result.Counts.items" />

`Counts.items() → a set-like object providing a view on D's items`

<span id="qiskit-result-counts-keys" />

### keys

<span id="qiskit.result.Counts.keys" />

`Counts.keys() → a set-like object providing a view on D's keys`

<span id="qiskit-result-counts-most-frequent" />

### most\_frequent

<span id="qiskit.result.Counts.most_frequent" />

`Counts.most_frequent()`

Return the most frequent count

**Returns**

The bit string for the most frequent result

**Return type**

str

**Raises**

**QiskitError** – when there is >1 count with the same max counts, or an empty object.

<span id="qiskit-result-counts-pop" />

### pop

<span id="qiskit.result.Counts.pop" />

`Counts.pop(k[, d]) → v, remove specified key and return the corresponding value.`

If key is not found, d is returned if given, otherwise KeyError is raised

<span id="qiskit-result-counts-popitem" />

### popitem

<span id="qiskit.result.Counts.popitem" />

`Counts.popitem()`

Remove and return a (key, value) pair as a 2-tuple.

Pairs are returned in LIFO (last-in, first-out) order. Raises KeyError if the dict is empty.

<span id="qiskit-result-counts-setdefault" />

### setdefault

<span id="qiskit.result.Counts.setdefault" />

`Counts.setdefault(key, default=None, /)`

Insert key with a value of default if key is not in the dictionary.

Return the value for key if key is in the dictionary, else default.

<span id="qiskit-result-counts-shots" />

### shots

<span id="qiskit.result.Counts.shots" />

`Counts.shots()`

Return the number of shots

<span id="qiskit-result-counts-update" />

### update

<span id="qiskit.result.Counts.update" />

`Counts.update([E, ]**F) → None.  Update D from dict/iterable E and F.`

If E is present and has a .keys() method, then does: for k in E: D\[k] = E\[k] If E is present and lacks a .keys() method, then does: for k, v in E: D\[k] = v In either case, this is followed by: for k in F: D\[k] = F\[k]

<span id="qiskit-result-counts-values" />

### values

<span id="qiskit.result.Counts.values" />

`Counts.values() → an object providing a view on D's values`

## Attributes

<span id="qiskit.result.Counts.bitstring_regex" />

### bitstring\_regex

`= re.compile('^[01\\s]+$')`
