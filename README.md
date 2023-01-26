# Umi-route-reproduce

## 步骤

1. `pnpm create umi`，选择 `simple app` 模板
2. 删除 `.umirc.ts` 里的 route，切换到约定式路由
3. 在 `src/pages` 下创建 `a-index/index.tsx`
4. `pnpm dev`
5. 打开 `/a-index`，提示没有 match 的 route
6. 访问 `/a-`，错误的显示了 `/a-index` 的内容

## 预期的结果

`src/pages/a-index/index.tsx` 生成的路由是 `/a-index` ，然而生成的是 `/a-`