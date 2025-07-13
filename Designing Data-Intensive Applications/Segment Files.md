Segment files have to deal with breaking apart one large file into separate smaller files.

Segment files are immutable and read only.

The reason why we do this is so that we can make sure any files that we are working on (ex. append only files) to be smaller and easier to work with.

After segmenting the files, we can compact the files by removing any duplicate values (or keys when dealing with log-structured databases) found in the file.

Ex. 
***The number next the value is the location/time the value was added***
*Data file segment:*
mew:1078; purr:2103; mew:1079; mew:1080; mew:1081; purr:2105; purr:2106; purr:2107; yawn:511; purr:2108; mew:1082

*Compacted segment:*
yawn:511; mew:1082; purr:2108

In the example above we are able to remove all of the duplicate values for yawn, mew and purr by only keeping track of the latest additions of these values (since in this example I am using an append-only file as an example, so all of the newer values are at the end of the line, and the oldest one are at the beginning).

We can also combine and merge multiple segment files at the same time since the files are created in order.

# Example
## 📄 File 1 (older segment)

| Line | Key  | Value |
| ---- | ---- | ----- |
| 1    | mew  | 1078  |
| 2    | purr | 2103  |
| 3    | mew  | 1079  |
| 4    | mew  | 1080  |
| 5    | mew  | 1081  |
| 6    | purr | 2105  |
| 7    | purr | 2106  |
| 8    | purr | 2107  |
| 9    | yawn | 511   |
| 10   | purr | 2108  |
| 11   | mew  | 1082  |

---

## 📄 File 2 (newer segment)

| Line | Key     | Value |
|------|---------|-------|
| 1    | purr    | 2109  |
| 2    | purr    | 2110  |
| 3    | mew     | 1083  |
| 4    | scratch | 252   |
| 5    | mew     | 1084  |
| 6    | mew     | 1085  |
| 7    | purr    | 2111  |
| 8    | mew     | 1086  |
| 9    | purr    | 2111  |
| 10   | mew     | 1086  |
| 11   | purr    | 2112  |
| 12   | purr    | 2113  |
| 13   | mew     | 1087  |
| 14   | purr    | 2114  |

---

## 🔄 Compaction Rules

- Start from **newest file** (File 2) and move backward.
- For each key, keep only the **last seen value**.
- Earlier duplicates (in the same or previous file) are **ignored**.

---

## ✅ Merged Output

| Key     | Final Value | Chosen From     |
| ------- | ----------- | --------------- |
| yawn    | 511         | File 1, line 9  |
| scratch | 252         | File 2, line 4  |
| mew     | 1087        | File 2, line 13 |
| purr    | 2114        | File 2, line 14 |

Another beautiful thing about Segment files comes with the fact that we can merge and compact files at the same time.

#databases #designing-data-intensive-applications-book 