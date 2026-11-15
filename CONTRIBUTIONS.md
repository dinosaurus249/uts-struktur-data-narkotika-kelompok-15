# Kontribusi Anggota – Kelompok 02

Dokumen ini mencatat kontribusi anggota dalam pengembangan project UTS Struktur Data mengenai Putusan Perkara Narkotika.

Daftar kontribusi disusun berdasarkan alur kerja Pull Request (PR) dan pembagian peran antara Ahmad Naufal Nasution dan Ramadani Dino Yulianto Saputra.

## Ringkasan Anggota

| Anggota | NIM | Peran Utama |
|---|---|---|
| **Ahmad Naufal Nasution** | `202510370110051` | ArrayStack, Model/Parser/CLI, Data P001–P025, Verifikasi P026–P050, Trace |
| **Ramadani Dino Yulianto Saputra** | `202510370110049` | SinglyLinkedList, Repository, Data P026–P050, Verifikasi P001–P025, Real-data tests, ADR + README |

---

## 1. Ahmad Naufal Nasution (202510370110051)

### Tanggung Jawab & Kontribusi Utama
- **Struktur Data & Implementasi:** Mengembangkan `ArrayStack` beserta unit testing terkait operasi LIFO, resize otomatis, dan pencarian/restore.
- **Model & Parser:** Mengimplementasikan kelas `Putusan`, `CsvUtil`, `PutusanParser`, dan `ImportResult` beserta validasinya.
- **CLI & Antarmuka:** Mengembangkan menu interaktif CLI di `Main.java` serta konfigurasi plugin pada `pom.xml`.
- **Ekstraksi & Verifikasi Data:** 
  - Melakukan ekstraksi dataset awal **P001–P025**.
  - Melakukan verifikasi data milik Dino (**P026–P050**).
- **Dokumentasi:** Menyusun dokumentasi trace dan demo (`docs/trace/`, `docs/demo/`).

---

## 2. Ramadani Dino Yulianto Saputra (202510370110049)

### Tanggung Jawab & Kontribusi Utama
- **Struktur Data & Implementasi:** Mengembangkan `StrukturData` interface, `SearchResult`, `SinglyLinkedList`, serta `SinglyLinkedListTest`.
- **Repository & Layanan Bisnis:** Mengimplementasikan `PutusanRepository`, `FilterCriteria`, `Ringkasan`, dan `PutusanRepositoryTest` (pencarian, filter, agregasi, sorting, audit, ekspor).
- **Ekstraksi & Verifikasi Data:** 
  - Melakukan ekstraksi dataset **P026–P050**.
  - Melakukan verifikasi data milik Naufal (**P001–P025**).
- **Pengujian & Dokumentasi:** 
  - Mengembangkan skenario pengujian data riil (`DataFileTest.java`, `RealDataScenarioTest.java`).
  - Menyusun dokumentasi Architecture Decision Record (`docs/adr/`) dan `README.md`.

---

## Alur Pull Request Berdasarkan Dependensi

| Order | Branch | Author → Reviewer | Fokus File | Deskripsi Perubahan |
|---|---|---|---|---|
| 1 | `feat/linked-list` | Dino → Naufal | `StrukturData.java`, `SearchResult.java`, `SinglyLinkedList.java`, `SinglyLinkedListTest.java` | Implementasi Linked List & SearchResult |
| 2 | `feat/array-stack` | Naufal → Dino | `ArrayStack.java`, `ArrayStackTest.java` | Implementasi struktur data Stack |
| 3 | `feat/model-parser` | Naufal → Dino | `Putusan.java`, `CsvUtil.java`, `PutusanParser.java`, `ImportResult.java` | Model data dan CSV Parser |
| 4 | `feat/repository` | Dino → Naufal | `PutusanRepository.java`, `FilterCriteria.java`, `Ringkasan.java`, `PutusanRepositoryTest.java` | Layanan repositori dan logika bisnis |
| 5 | `feat/cli` | Naufal → Dino | `Main.java`, `pom.xml` | Antarmuka command line interaktif |
| 6 | `data/p001-p025` | Naufal → Dino | `data/putusan-50.csv`, `docs/data-provenance.csv` | Dataset perkara P001–P025 |
| 7 | `data/p026-p050` | Dino → Naufal | `data/putusan-50.csv` | Dataset perkara P026–P050 |
| 8 | `test/real-data` | Dino → Naufal | `DataFileTest.java`, `RealDataScenarioTest.java` | Pengujian skenario data riil |
| 9 | `tools/pdf-extractor` | Naufal → Dino | `uts/tools/*`, PDFBox dependency | Alat bantu ekstraksi PDF opsional |
| 10 | `docs/adr-readme` | Dino → Naufal | `docs/adr/*`, `README.md` | Dokumentasi ADR dan panduan utama |
| 11 | `docs/trace-demo` | Naufal → Dino | `docs/trace/*`, `docs/demo/*` | Dokumentasi pelacakan dan demo |
| 12 | `data/verify-p001-p025` | Naufal → Dino | Berkas data P001–P025 | Naufal memverifikasi data yang diekstrak Dino |
| 13 | `data/verify-p026-p050` | Dino → Naufal | Berkas data P026–P050 | Dino memverifikasi data yang diekstrak Naufal |
| 14 | `docs/ai-usage` | Masing-masing | `AI_USAGE.md` | Catatan penggunaan AI oleh tiap anggota |
| 15 | `docs/contributions` | Bersama | `CONTRIBUTIONS.md` | Dokumen ringkasan kontribusi akhir |

---

## Catatan Tambahan

- Setiap Pull Request melalui proses review silang (peer review) yang ketat antar anggota kelompok sesuai tabel dependensi di atas.
- Riwayat commit dan kontribusi teknis terdokumentasi secara transparan di dalam log repository GitHub kelompok.
