# Auto Bencher 自動 Benchmark 君

## 功能

- `auto-bencher init-env`
    - 初始化與檢察環境
- `auto-bencher execute-cmd [CMD]`
    - 執行給定指令 `CMD`
- `auto-bencher load [bench type] [# of nodes]`
    - 為給定數量的機器跑載入資料
- `auto-bencher check-ready [# of nodes]`
    - 檢查環境是否該有的東西都有，包括 benchmark 的資料都準備好了
- `auto-bencher bench [parameter file]`
    - 用給定的參數跑 benchmarks

### 期望功能

- 能夠自動抓取 properties 產生 parameter file
- 能夠合併 csv report，並另外產生一個 total summary 的 csv
- log 先產生在外面，等到跑完之後再一併放回 results
- CPU 監測及即時繪圖
- throughput 即時繪圖
- 提供一個功能是在每個 stage 安插指令
- 應該在 loading 時提供要 load 的機器數，config 只能設定總共有幾台機器
- 只需要在一個 mapping table 內加入 tunable parameter，就可以自動產生 properties files
- 就算沒跑完也要把 client report 或是 benchmark report 拉回來