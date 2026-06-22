# 📋 Kategorisasi Skenario Automation Testing (Maestro)

> Dokumen ini memuat daftar lengkap 71 test case automation dari repository Work Fusion beserta kategorisasinya berdasarkan teknik pengujian perangkat lunak (Test Method).

## Legenda Kategori Test Method

| # | Kategori | Deskripsi Singkat |
|:---:|---|---|
| 1 | **Gorilla Testing** | Modul yang sama diuji berulang kali untuk memastikan tidak ada bug. |
| 2 | **Monkey Testing** | Testing tanpa test case tertarget, interaksi random. |
| 3 | **Ad-Hoc Testing** | Pengujian berbasis *error guessing* dan pengalaman tester. |
| 4 | **Smoke Testing** | Menguji modul-modul kritikal yang berdampak besar (happy paths). |
| 5 | **Sanity Testing** | Menguji modul prasyarat atau alur navigasi antar halaman. |
| 6 | **Equivalence Partitioning** | Partisi domain input dan filter (contoh: valid vs invalid, rentang tanggal). |
| 7 | **Boundary Value Analysis** | Memilih batas atas/bawah (contoh: empty state validation). |
| 8 | **Depth Testing** | Pengujian alur fungsional spesifik secara mendalam (contoh: pencarian, edit spesifik). |
| 9 | **Breadth Testing** | Pengujian modul secara melebar sebelum lebih mendalam. |
| 10 | **All-Pairs Testing** | Menguji semua kemungkinan kombinasi diskrit parameter input. |

---

## 🔐 Modul Auth

| Test Case ID | Test Title | Test Method | Test Type | Test Technique | McCall Quality | Priority | Status |
|:---:|---|---|---|---|---|:---:|:---:|
| WF-AUT-001 | Supervisor Login Success | **Smoke Testing** | Positive Testing | Black Box | 1. Correctness | High | ✅ Pass |
| WF-AUT-002 | Verify Login Page Elements | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-AUT-003 | Verify Webview Auth Opens | **Depth Testing** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-AUT-004 | Worker Login Empty Password | **Equivalence Partitioning** | Negative Testing | Black Box | 2. Reliability | High | ✅ Pass |
| WF-AUT-005 | Worker Login Empty Username | **Equivalence Partitioning** | Negative Testing | Black Box | 2. Reliability | High | ✅ Pass |
| WF-AUT-006 | Worker Login Invalid Credentials | **Equivalence Partitioning** | Negative Testing | Black Box | 2. Reliability | High | ✅ Pass |
| WF-AUT-007 | Worker Login Success | **Smoke Testing** | Positive Testing | Black Box | 1. Correctness | High | ✅ Pass |
| WF-AUT-008 | Worker Logout | **Smoke Testing** | Positive Testing | Black Box | 1. Correctness | High | ✅ Pass |

> **Total Tests:** 8

---

## 🏠 Modul Home

| Test Case ID | Test Title | Test Method | Test Type | Test Technique | McCall Quality | Priority | Status |
|:---:|---|---|---|---|---|:---:|:---:|
| WF-HOM-001 | Apply Custom Range Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-HOM-002 | Apply This Month Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-HOM-003 | Apply This Week Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-HOM-004 | Apply Today Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-HOM-005 | Apply Yesterday Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-HOM-006 | Cancel Overview Filter | **Ad-Hoc Testing** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-HOM-007 | Navigate To My Task Via Link | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-HOM-008 | Open Overview Filter | **Ad-Hoc Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-HOM-009 | Verify Bottom Navigation | **Sanity Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-HOM-010 | Verify Greeting Header | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-HOM-011 | Verify Today Task Section | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-HOM-012 | Verify Work Overview Section | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |

> **Total Tests:** 12

---

## 📊 Modul Monitoring

| Test Case ID | Test Title | Test Method | Test Type | Test Technique | McCall Quality | Priority | Status |
|:---:|---|---|---|---|---|:---:|:---:|
| WF-MON-001 | Verify Monitoring Hidden For Worker | **Sanity Testing** | Negative Testing | Black Box | 2. Reliability | High | ✅ Pass |
| WF-MON-002 | Verify Monitoring Page Header | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-MON-003 | Verify Monitoring Tab Visible Supervisor | **Sanity Testing** | UI Verification | Black Box | 1. Correctness | High | ✅ Pass |
| WF-MON-004 | Verify Supervisor Overview Stats | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |

> **Total Tests:** 4

---

## 📋 Modul My Task

| Test Case ID | Test Title | Test Method | Test Type | Test Technique | McCall Quality | Priority | Status |
|:---:|---|---|---|---|---|:---:|:---:|
| WF-TSK-001 | Close Due Date Filter Via Close Button | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-002 | Close Priority Filter Via Close Button | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-003 | Close Status Filter Via Close Button | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-004 | Open Due Date Filter | **Ad-Hoc Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-005 | Open Priority Filter | **Ad-Hoc Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-006 | Open Status Filter Bottom Sheet Via First Filter | **Ad-Hoc Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-007 | Reset Priority Filter To All Priority | **Ad-Hoc Testing** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-008 | Reset Status Filter To All Task | **Ad-Hoc Testing** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-009 | Select Custom Range From Due Date Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-010 | Select Draft Task From Status Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-011 | Select Low Task From Priority Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-012 | Select Need Approval From Status Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-013 | Select Overdue Task From Status Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-014 | Select Pending Task From Status Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-015 | Select This Month From Due Date Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-016 | Select This Week From Due Date Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-017 | Select Today From Due Date Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-018 | Select Urgent Task From Priority Filter | **Equivalence Partitioning** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-019 | Verify Correct Header | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-TSK-020 | Verify Default Tab | **Sanity Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-TSK-021 | Verify Done Tab Empty State | **Boundary Value Analysis** | UI Verification | Black Box | 2. Reliability | Medium | ✅ Pass |
| WF-TSK-022 | Verify Done Tab Task List | **Depth Testing** | UI Verification | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-023 | Verify Empty State For Ongoing Tab | **Boundary Value Analysis** | UI Verification | Black Box | 2. Reliability | Medium | ✅ Pass |
| WF-TSK-024 | Verify Filter Button Area Renders | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-TSK-025 | Verify Ongoing Tab | **Depth Testing** | UI Verification | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-026 | Verify Search Functionality | **Depth Testing** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-TSK-027 | Verify Search Input Field Is Visible | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-TSK-028 | Verify Switching To Done Tab | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |

> **Total Tests:** 28

---

## 🔔 Modul Notification

| Test Case ID | Test Title | Test Method | Test Type | Test Technique | McCall Quality | Priority | Status |
|:---:|---|---|---|---|---|:---:|:---:|
| WF-NOT-001 | Switch To Unread Tab | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-NOT-002 | Switch To View All Tab | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-NOT-003 | Tap Mark All Read | **Depth Testing** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-NOT-004 | Verify Mark All Read Button | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-NOT-005 | Verify Notification Page Header | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-NOT-006 | Verify Notification Tabs | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |

> **Total Tests:** 6

---

## 👤 Modul Profile

| Test Case ID | Test Title | Test Method | Test Type | Test Technique | McCall Quality | Priority | Status |
|:---:|---|---|---|---|---|:---:|:---:|
| WF-PRO-001 | Back From Change Password | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-PRO-002 | Back From Update Profile | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-PRO-003 | Edit Profile Name And Save | **Depth Testing** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-PRO-004 | Navigate To Change Password | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-PRO-005 | Navigate To Edit Profile | **Sanity Testing** | Navigation | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-PRO-006 | Verify Account Section Menu | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-PRO-007 | Verify Change Password Elements | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-PRO-008 | Verify General Section Menu | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-PRO-009 | Verify Language Toggle | **Depth Testing** | Positive Testing | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-PRO-010 | Verify Profile Info Display | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-PRO-011 | Verify Profile Page Header | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |
| WF-PRO-012 | Verify Update Picture Options | **Depth Testing** | UI Verification | Black Box | 1. Correctness | Medium | ✅ Pass |
| WF-PRO-013 | Verify Update Profile Elements | **Ad-Hoc Testing** | UI Verification | Black Box | 3. Usability | Medium | ✅ Pass |

> **Total Tests:** 13

---

## 📊 Rekapitulasi Metode Testing

| Test Method | Jumlah | Persentase |
|---|:---:|:---:|
| **Ad-Hoc Testing** | 22 | 31.0% |
| **Equivalence Partitioning** | 18 | 25.4% |
| **Sanity Testing** | 17 | 23.9% |
| **Depth Testing** | 9 | 12.7% |
| **Smoke Testing** | 3 | 4.2% |
| **Boundary Value Analysis** | 2 | 2.8% |
| **Total** | **71** | **100%** |
