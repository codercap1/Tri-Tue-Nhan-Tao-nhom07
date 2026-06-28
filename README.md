# 8-Puzzle Solver

Do an mon Tri tue nhan tao: chuong trinh giai bai toan 8-puzzle bang nhieu nhom thuat toan tim kiem, heuristic search, local search, belief state va CSP.

File chinh cua project:

- `8puzzle_game.ipynb`: notebook chua toan bo code va giao dien Tkinter.

## Cach chay

1. Mo `8puzzle_game.ipynb` bang Jupyter Notebook, JupyterLab hoac VS Code.
2. Chay cell code chinh cua notebook.
3. Cua so `8-Puzzle Solver` se hien ra.
4. Chon thuat toan trong dropdown.
5. Bam `Random` de tao trang thai moi.
6. Bam `Start` de tim loi giai va xem animation.

Project chi dung thu vien Python co san:

- `tkinter`
- `heapq`
- `random`
- `time`
- `threading`
- `collections`
- `math`

## Bai toan

Trang thai dich mac dinh:

```text
1 2 3
4 5 6
7 8 0
```

Trong do `0` la o trong. Moi buoc di chuyen la di chuyen o trong len, xuong, trai hoac phai neu hop le.

## Cac thuat toan da cai dat

### Tim kiem khong thong tin

- `BFS`: tim kiem theo chieu rong, dam bao loi giai ngan nhat khi moi buoc co cost bang 1.
- `DFS`: tim kiem theo chieu sau co gioi han do sau, khong dam bao toi uu.
- `IDS`: iterative deepening search, lap depth-limited search voi do sau tang dan.
- `UCS`: uniform cost search, voi 8-puzzle cost moi buoc bang 1 nen tuong duong BFS ve do dai loi giai.

### Tim kiem co heuristic

- `Greedy`: uu tien trang thai co heuristic Manhattan nho nhat.
- `A*`: dung `f(n) = g(n) + h(n)`, trong do `g(n)` la chi phi duong di va `h(n)` la Euclidean.
- `IDA*`: ket hop iterative deepening va A*, dung threshold theo `g + h`.

### Local search

- `Hill Climbing`
- `Stochastic HC`
- `Steepest HC`
- `Random Restart HC`
- `Local Beam`
- `Simulated Annealing`

Luu y: cac thuat toan local search co the bi ket cuc bo hoac that bai tuy trang thai va yeu to ngau nhien. Day la dac diem cua nhom thuat toan nay, khong phai luc nao cung dam bao tim duoc loi giai.

### Belief / observation search

- `Belief State`: tim kiem tren tap cac trang thai co the co.
- `Sensorless`: tac nhan khong quan sat duoc gi, ap cung mot action len toan bo belief state.
- `Partial Obs`: tac nhan chi quan sat mot phan trang thai, hien tai la 4 o goc cua puzzle.
- `AND-OR Search`: mo phong AND-OR graph search. Voi 8-puzzle moi action co mot ket qua, nen phan AND chi mang tinh minh hoa cau truc thuat toan.

### CSP-style search

- `Backtracking`
- `Forward Checking`
- `AC-3`
- `Min-Conflicts`

Luu y: 8-puzzle khong phai la bai toan CSP co dinh theo nghia truyen thong. Cac thuat toan tren duoc ap dung theo huong mo hinh hoa chuoi hanh dong va rang buoc khong lap lai trang thai, phu hop de minh hoa y tuong CSP trong bai 8-puzzle.

## Kiem tra tinh hop le cua puzzle

Notebook co ham `is_solvable(state)` de kiem tra trang thai co giai duoc hay khong bang so nghich the. Ham `random_solvable_state()` chi sinh cac trang thai giai duoc.

## Ghi chu

- Cac thuat toan nhu `BFS`, `UCS`, `IDS`, `A*`, `IDA*` phu hop de so sanh loi giai toi uu/ngan.
- Cac thuat toan local search phu hop de minh hoa cach di theo heuristic, nhung co the khong tim ra loi giai.
- Cac thuat toan CSP va belief state chu yeu dung de minh hoa cach mo hinh hoa khac nhau cua bai toan.
