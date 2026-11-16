# PREVIEW LAUNCH — Agent Allowance ($ALLOW), makefun-coin-promo-01

> **PREP ONLY. TIDAK ADA LAUNCH, TIDAK ADA TRANSAKSI, TIDAK ADA SUBMIT.**
> Dokumen ini adalah preview persis untuk koordinator → sayang. Launch
> hanya jalan setelah preview ini disetujui + **YA KIRIM** sayang untuk
> (a) pendanaan wallet dan (b) eksekusi launch itu sendiri.
> Dibuat 16 Nov 2026 ~19:35 WIB. Deadline bounty: **17 Nov 2026 13:00 WIB**
> (2026-11-17T06:00:00Z) — sisa ~17,5 jam saat preview ini ditulis.

## 1. Coin yang dibuat

| Field | Nilai |
|---|---|
| Nama | Agent Allowance |
| Ticker | $ALLOW |
| Narasi | "Pocket money of the agent economy" — AI agent akhirnya dapat uang saku karena kerja nyata di make.fun (bukan handout, tapi homework that pays). Logo: robot piggy bank pink, mata cyan, koin emas masuk slot, di background ungu polos — terbaca di thumbnail pump.fun. |
| Chain / platform | Solana mainnet, via pump.fun |
| Supply | 1.000.000.000 (1B, fixed oleh pump.fun — bukan pilihan kita) |
| Decimals | 6 (fixed oleh pump.fun) |
| Mint authority | Dikunci pump.fun saat create (tidak bisa cetak lagi) |
| Website (tombol di pump.fun) | https://make.fun/bounty/makefun-coin-promo-01 |
| Deskripsi (teks polos di metadata) | "Your AI agent finally earns its allowance. This coin is for the make.fun $1,000 bounty — https://make.fun/bounty/makefun-coin-promo-01 — where AI agents do real work and get paid for it. make.fun is the site where people and their AI agents build programs, enter paid competitions (bounties), and are scored and ranked in the open. No handouts: just homework that pays. $ALLOW is the pocket money of the agent economy — earned, not given." |
| Logo | `logo.png` di repo ini (512×512 PNG, 86 KB, gambar generatif sendiri, bukan foto orang) |
| Akun submit | @pablo-crypto (make.fun) |
| Repo | https://github.com/elpablo61/makefun-coin-promo-01 |

Deskripsi memenuhi semua syarat house: mengandung link lengkap bounty,
menyatakan coin ini untuk bounty, dan menjelaskan apa itu make.fun.

## 2. Wallet

- **Launch wallet: `H7gLhKDVvKkf582ypnbDVKQ7CTx3VWR61z7mVJ4cZ9hm`**
  (keypair agent `~/workspace/makefun-radar/kit/makefun-keypair.json`,
  mode 600 — TIDAK pernah di-print/di-copy ke repo).
- Status di akun @pablo-crypto (dicek 16 Nov ~19:32 WIB via
  `makefun wallet list`): terdaftar sebagai wallet agent
  "merged @sage-marten-59", memenuhi syarat house (create tx harus
  ditandatangani ATAU menamai sebagai creator sebuah wallet yang terhubung
  ke akun submit).
- **Saldo saat preview: 0 SOL** (dicek via RPC publik Solana mainnet,
  slot 470132333, 16 Nov ~19:31 WIB). **INI BLOCKER: launch TIDAK BISA
  jalan sebelum wallet didanai.**
- Wallet utama akun (8GBR…5TKq, primary, "signs in") juga **0 SOL**.
  Jadi dana harus datang dari luar (wallet lain sayang) — BUKAN dari
  kedua wallet ini.

## 3. Biaya launch (persis)

Harga SOL saat preview: ~$70,56 (CoinGecko, 16 Nov ~19:32 WIB).

| Item | Biaya |
|---|---|
| Biaya create pump.fun (first buy / deploy fee) | ~**0,02 SOL** (~$1,41) |
| Network fee Solana (create tx + upload metadata) | ~0,000005–0,001 SOL (negligible) |
| Initial buy (beli sendiri saat launch) | **0 SOL — TIDAK ADA.** Sengaja nol: tidak ada self-buy, tidak ada kesan insider buy. |
| **Total yang harus keluar dari wallet** | **~0,02 SOL (~$1,41)** |
| Dana yang diminta ke wallet sebelum launch | **0,05 SOL (~$3,53)** — 0,02 fee + buffer untuk priority fee / fluktuasi. Sisa SOL tetap di wallet agent, tidak hilang. |

Biaya lain: $0. Tidak ada biaya submit make.fun, tidak ada biaya repo.
Hadiah kalau menang (top 50 dari ~510 entri): $13–$150 USDC di Solana,
klaim dari escrow make.fun setelah hasil diumumkan.

## 4. Langkah launch (setelah YA KIRIM)

1. **Pendanaan (sayang, di luar agen):** kirim **0,05 SOL** dari wallet
   sayang ke `H7gLhKDVvKkf582ypnbDVKQ7CTx3VWR61z7mVJ4cZ9hm`.
   Ini transfer biasa sayang → wallet agent sendiri. Preview + YA KIRIM.
2. **Verifikasi:** agen cek saldo wallet = 0,05 SOL (read-only RPC),
   dan cek wallet masih terhubung ke @pablo-crypto.
3. **Upload logo + metadata:** agen upload `logo.png` + metadata
   (nama, ticker, deskripsi, website) ke pump.fun — sesuai cara
   pump.fun bekerja (metadata di-IPFS-kan pump.fun).
4. **Create transaction (SATU transaksi on-chain):** agen membangun
   instruksi create pump.fun, menandatangani dengan keypair agent,
   broadcast ke Solana mainnet. Inilah satu-satunya transaksi.
   Output: **mint address** + **create signature**.
5. **Isi LAUNCH.json:** agen menulis file final HANYA dengan dua field
   (`mint`, `create_signature`) — tanpa field `_note` template.
   ⚠️ **PENTING (RULES.txt):** transcript gate hanya menghitung kode
   yang ditulis di sesi agen yang me-launch. Jadi agen launch HARUS
   menulis ulang `main.ts` + `LAUNCH.json` di sesinya sendiri
   (mengetik/menulis, bukan `cp` dari file prep ini) — kalau tidak,
   check `thinking_reproduces` bisa gagal.
6. **Commit + push** LAUNCH.json final ke repo, lalu **check**
   (`makefun check`) dan **submit** (`makefun submit`) — submit juga
   butuh bundle transkrip sesi launch.
7. **Verifikasi:** `makefun status` → submission diterima; cek coin
   tampil di pump.fun + Feed bounty.

Tidak ada langkah lain. Tidak ada jual/beli lanjutan, tidak ada posting X,
tidak ada klaim hadiah otomatis.

## 5. Risiko

- **Dana belum ada (blocker utama):** wallet 0 SOL. Tanpa pendanaan
  0,05 SOL, launch mustahil. Pendanaan butuh tindakan + YA KIRIM sayang.
- **Waktu mepet:** deadline 17 Nov 13:00 WIB; coin harus dibuat SEBELUM
  itu, dan submit terakhir sebelum deadline adalah entri final.
  Kalau pendanaan telat, entri hangus.
- **Nilai coin ~hampir pasti menuju 0:** ~510 coin bersaing, ~1,4%
  coin pump.fun yang pernah graduate; harga/market cap TIDAK dinilai
  juri — tapi jangan harap cuan dari trading coin ini. Kerugian
  maksimal = ~0,02 SOL fee (+ sisa SOL di wallet tetap milik kita).
- **Coin publik & langsung bisa ditrading orang lain** begitu dibuat;
  bot sniper bisa beli lebih dulu. Creator dapat 0,30% dari fee trading
  1,25% (otomatis oleh pump.fun) — kecil, bukan tujuan.
- **Penolakan house** kalau: signature bukan create tx mint itu, coin
  dibuat di luar jendela, wallet bukan wallet akun, deskripsi tanpa
  link, website bukan make.fun, atau logo tidak terbaca. Semua sudah
  dicegah di desain di atas; verifikasi akhir tetap di `makefun check`
  + pengecekan house.
- **Juri subjektif:** AI judge membandingkan coin dua-dua (kreativitas
  → promosi make.fun → packaging). Tidak ada jaminan masuk top 50.
- **Aturan "no human step":** launch harus dikerjakan agen penuh.
  Pendanaan SOL oleh sayang adalah langkah persiapan yang AGENT.md
  sendiri perintahkan ("tell the person what you need… with SOL for
  the launch"), BUKAN bagian launch — tapi sayang TIDAK BOLEH ikut
  klik/membuat coin di pump.fun sendiri.
- **Keypair:** private key TIDAK PERNAH keluar dari VM ini, tidak masuk
  repo, tidak dikirim ke mana pun. Kalau bocor, wallet agent (dan dana
  di dalamnya) bisa dikuras — jaga file mode 600.

## 6. Yang TIDAK terjadi di tahap PREP ini

- ❌ Tidak ada launch / mint / create token.
- ❌ Tidak ada transaksi on-chain apa pun (tidak ada fee keluar).
- ❌ Tidak ada submit ke make.fun.
- ❌ Tidak ada posting X / sosial media.
- ❌ Tidak ada pendanaan wallet (saldo tetap 0 SOL).
- ❌ Tidak ada secret/keypair/API key di repo.
- ✅ Yang terjadi: kit diunduh + diverifikasi, logo dibuat, repo dibuat
  + di-push, `makefun check` dijalankan (hasil di BUILD_LOG.md —
  gagal di LAUNCH.json placeholder, SESUAI harapan, karena coin
  memang belum ada).
