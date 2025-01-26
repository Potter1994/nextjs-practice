## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

# 學習筆記

- 4. app route 在 app folder 底下的 folder 只有 folder 內的 page file 會是公開的

- 4. layout.tsx 可以接收 children 把同層或底下 page.tsx 或者底下的 layout.ts 當作 children 傳入

- 5. Link 可以不用整個頁面重新載入，如果在 production environment 下 viewport 有看到 Link 的 Next.js 還會自動 prefetch code for the linked route in the background

- 678. 都是在講解 React Server Components 的觀念

- 9. Next.js 資料夾用 (group name) 來分組，並且不影響 URL 的路徑名稱 (可能 layout、loading 不同, 方便群組分開使用)

使用 Suspense 來針對 api 特別久的 component 做處理，fallback 用 loading 的 Skeleton (骨架) 來讓它看起來像在載入不是空等 (或許可以每個使用 api 的都用 Suspense 來包)

- Where you place your Suspense boundaries will depend on a few things:

1. How you want the user to experience the page as it streams.
2. What content you want to prioritize.
3. If the components rely on data fetching.

如果頁面內容較少，建議直接流式載入整個頁面。
如果頁面有大量內容，考慮分區載入（Staggered Effect），以優化使用者體驗。
針對需要即時更新的部分（例如訂單、通知），可以單獨載入該區塊。
