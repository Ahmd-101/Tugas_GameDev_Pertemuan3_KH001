# Solusi Tower of Hanoi Menggunakan Algoritma Best-First Search

Repository ini berisi penyelesaian teka-teki **Tower of Hanoi (3 Cakram)** menggunakan algoritma **Best-First Search** dengan bahasa pemrograman Python.

## Deskripsi Program
Permainan Tower of Hanoi dimodelkan ke dalam struktur **Graf Ruang Keadaan (State Space Graph)**:
- **Node (Vertex)**: Memuat kombinasi posisi cakram di Tiang A, Tiang B, dan Tiang C.
- **Edge**: Gerakan pemindahan cakram yang sah sesuai aturan dasar Hanoi.

## Aturan Heuristik f(n) = h(n)
Pencarian memanfaatkan fungsi heuristik untuk mengevaluasi bobot langkah:
- **Formula**: `h = sum(Tiang_A) + sum(Tiang_B)`
- **Penjelasan**: Menghitung akumulasi nilai cakram yang belum sampai di Tiang C (Target). Algoritma menggunakan Priority Queue (`heapq`) untuk memprioritaskan state dengan nilai h terkecil mendekati 0.

## Cara Kerja Algoritma
1. `get_neighbors()`: Mencari semua kemungkinan perpindahan cakram yang valid.
2. `best_first_search_sederhana()`: Menelusuri jalur terbaik menggunakan `heapq` berdasarkan nilai heuristik terkecil.
3. Menampilkan urutan langkah dari `Start` hingga `Finish` secara otomatis.
