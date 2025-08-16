# CIS Compliance Report for db_node01

**Date:** 2025-08-16
**Mode:** audit



---

## Summary of Security Configurations
- Password Aging: [, ', P, A, S, S, _, M, A, X, _, D, A, Y, S, \, t, 9, 0, ', ,,  , ', P, A, S, S, _, M, I, N, _, D, A, Y, S, \, t, 1, ', ,,  , ', P, A, S, S, _, W, A, R, N, _, A, G, E, \, t, 7, ', ]
- Password Quality: [, ', m, i, n, l, e, n,  , =,  , 1, 2, ', ,,  , ', d, c, r, e, d, i, t,  , =,  , -, 1, ', ,,  , ', u, c, r, e, d, i, t,  , =,  , -, 1, ', ,,  , ', l, c, r, e, d, i, t,  , =,  , -, 1, ', ,,  , ', o, c, r, e, d, i, t,  , =,  , -, 1, ', ,,  , ', r, e, t, r, y,  , =,  , 3, ', ]
- SSHD Config: [, ', p, o, r, t,  , 2, 2, ', ,,  , ', a, d, d, r, e, s, s, f, a, m, i, l, y,  , a, n, y, ', ,,  , ', l, i, s, t, e, n, a, d, d, r, e, s, s,  , [, :, :, ], :, 2, 2, ', ,,  , ', l, i, s, t, e, n, a, d, d, r, e, s, s,  , 0, ., 0, ., 0, ., 0, :, 2, 2, ', ,,  , ', u, s, e, p, a, m,  , n, o, ', ,,  , ', l, o, g, i, n, g, r, a, c, e, t, i, m, e,  , 1, 2, 0, ', ,,  , ', x, 1, 1, d, i, s, p, l, a, y, o, f, f, s, e, t,  , 1, 0, ', ,,  , ', m, a, x, a, u, t, h, t, r, i, e, s,  , 4, ', ,,  , ', m, a, x, s, e, s, s, i, o, n, s,  , 1, 0, ', ,,  , ', c, l, i, e, n, t, a, l, i, v, e, i, n, t, e, r, v, a, l,  , 3, 0, 0, ', ,,  , ', c, l, i, e, n, t, a, l, i, v, e, c, o, u, n, t, m, a, x,  , 3, ', ,,  , ', r, e, q, u, i, r, e, d, r, s, a, s, i, z, e,  , 1, 0, 2, 4, ', ,,  , ', s, t, r, e, a, m, l, o, c, a, l, b, i, n, d, m, a, s, k,  , 0, 1, 7, 7, ', ,,  , ', u, n, u, s, e, d, c, o, n, n, e, c, t, i, o, n, t, i, m, e, o, u, t,  , n, o, n, e, ', ,,  , ', p, e, r, m, i, t, r, o, o, t, l, o, g, i, n,  , n, o, ', ,,  , ', i, g, n, o, r, e, r, h, o, s, t, s,  , y, e, s, ', ,,  , ', i, g, n, o, r, e, u, s, e, r, k, n, o, w, n, h, o, s, t, s,  , n, o, ', ,,  , ', h, o, s, t, b, a, s, e, d, a, u, t, h, e, n, t, i, c, a, t, i, o, n,  , n, o, ', ,,  , ', h, o, s, t, b, a, s, e, d, u, s, e, s, n, a, m, e, f, r, o, m, p, a, c, k, e, t, o, n, l, y,  , n, o, ', ,,  , ', p, u, b, k, e, y, a, u, t, h, e, n, t, i, c, a, t, i, o, n,  , y, e, s, ', ,,  , ', k, e, r, b, e, r, o, s, a, u, t, h, e, n, t, i, c, a, t, i, o, n,  , y, e, s, ', ,,  , ', k, e, r, b, e, r, o, s, o, r, l, o, c, a, l, p, a, s, s, w, d,  , y, e, s, ', ,,  , ', k, e, r, b, e, r, o, s, t, i, c, k, e, t, c, l, e, a, n, u, p,  , y, e, s, ', ,,  , ', g, s, s, a, p, i, a, u, t, h, e, n, t, i, c, a, t, i, o, n,  , n, o, ', ,,  , ', g, s, s, a, p, i, c, l, e, a, n, u, p, c, r, e, d, e, n, t, i, a, l, s,  , y, e, s, ', ,,  , ', g, s, s, a, p, i, k, e, y, e, x, c, h, a, n, g, e,  , n, o, ', ,,  , ', g, s, s, a, p, i, s, t, r, i, c, t, a, c, c, e, p, t, o, r, c, h, e, c, k,  , y, e, s, ', ,,  , ', g, s, s, a, p, i, s, t, o, r, e, c, r, e, d, e, n, t, i, a, l, s, o, n, r, e, k, e, y,  , n, o, ', ,,  , ', g, s, s, a, p, i, k, e, x, a, l, g, o, r, i, t, h, m, s,  , g, s, s, -, g, r, o, u, p, 1, 4, -, s, h, a, 2, 5, 6, -, ,, g, s, s, -, g, r, o, u, p, 1, 6, -, s, h, a, 5, 1, 2, -, ,, g, s, s, -, n, i, s, t, p, 2, 5, 6, -, s, h, a, 2, 5, 6, -, ,, g, s, s, -, c, u, r, v, e, 2, 5, 5, 1, 9, -, s, h, a, 2, 5, 6, -, ,, g, s, s, -, g, r, o, u, p, 1, 4, -, s, h, a, 1, -, ,, g, s, s, -, g, e, x, -, s, h, a, 1, -, ', ,,  , ', p, a, s, s, w, o, r, d, a, u, t, h, e, n, t, i, c, a, t, i, o, n,  , n, o, ', ,,  , ', k, b, d, i, n, t, e, r, a, c, t, i, v, e, a, u, t, h, e, n, t, i, c, a, t, i, o, n,  , n, o, ', ,,  , ', p, r, i, n, t, m, o, t, d,  , n, o, ', ,,  , ', p, r, i, n, t, l, a, s, t, l, o, g,  , y, e, s, ', ,,  , ', x, 1, 1, f, o, r, w, a, r, d, i, n, g,  , n, o, ', ,,  , ', x, 1, 1, u, s, e, l, o, c, a, l, h, o, s, t,  , y, e, s, ', ,,  , ', p, e, r, m, i, t, t, t, y,  , y, e, s, ', ,,  , ', p, e, r, m, i, t, u, s, e, r, r, c,  , y, e, s, ', ,,  , ', s, t, r, i, c, t, m, o, d, e, s,  , y, e, s, ', ,,  , ', t, c, p, k, e, e, p, a, l, i, v, e,  , y, e, s, ', ,,  , ', p, e, r, m, i, t, e, m, p, t, y, p, a, s, s, w, o, r, d, s,  , n, o, ', ,,  , ', c, o, m, p, r, e, s, s, i, o, n,  , y, e, s, ', ,,  , ', g, a, t, e, w, a, y, p, o, r, t, s,  , n, o, ', ,,  , ', u, s, e, d, n, s,  , n, o, ', ,,  , ', a, l, l, o, w, t, c, p, f, o, r, w, a, r, d, i, n, g,  , y, e, s, ', ,,  , ', a, l, l, o, w, a, g, e, n, t, f, o, r, w, a, r, d, i, n, g,  , y, e, s, ', ,,  , ', d, i, s, a, b, l, e, f, o, r, w, a, r, d, i, n, g,  , n, o, ', ,,  , ', a, l, l, o, w, s, t, r, e, a, m, l, o, c, a, l, f, o, r, w, a, r, d, i, n, g,  , y, e, s, ', ,,  , ', s, t, r, e, a, m, l, o, c, a, l, b, i, n, d, u, n, l, i, n, k,  , n, o, ', ,,  , ', f, i, n, g, e, r, p, r, i, n, t, h, a, s, h,  , s, h, a, 2, 5, 6, ', ,,  , ', e, x, p, o, s, e, a, u, t, h, i, n, f, o,  , n, o, ', ,,  , ', d, e, b, i, a, n, b, a, n, n, e, r,  , y, e, s, ', ,,  , ', p, i, d, f, i, l, e,  , /, r, u, n, /, s, s, h, d, ., p, i, d, ', ,,  , ', m, o, d, u, l, i, f, i, l, e,  , /, e, t, c, /, s, s, h, /, m, o, d, u, l, i, ', ,,  , ', x, a, u, t, h, l, o, c, a, t, i, o, n,  , /, u, s, r, /, b, i, n, /, x, a, u, t, h, ', ,,  , ', c, i, p, h, e, r, s,  , c, h, a, c, h, a, 2, 0, -, p, o, l, y, 1, 3, 0, 5, @, o, p, e, n, s, s, h, ., c, o, m, ,, a, e, s, 1, 2, 8, -, c, t, r, ,, a, e, s, 1, 9, 2, -, c, t, r, ,, a, e, s, 2, 5, 6, -, c, t, r, ,, a, e, s, 1, 2, 8, -, g, c, m, @, o, p, e, n, s, s, h, ., c, o, m, ,, a, e, s, 2, 5, 6, -, g, c, m, @, o, p, e, n, s, s, h, ., c, o, m, ', ,,  , ', m, a, c, s,  , u, m, a, c, -, 6, 4, -, e, t, m, @, o, p, e, n, s, s, h, ., c, o, m, ,, u, m, a, c, -, 1, 2, 8, -, e, t, m, @, o, p, e, n, s, s, h, ., c, o, m, ,, h, m, a, c, -, s, h, a, 2, -, 2, 5, 6, -, e, t, m, @, o, p, e, n, s, s, h, ., c, o, m, ,, h, m, a, c, -, s, h, a, 2, -, 5, 1, 2, -, e, t, m, @, o, p, e, n, s, s, h, ., c, o, m, ,, h, m, a, c, -, s, h, a, 1, -, e, t, m, @, o, p, e, n, s, s, h, ., c, o, m, ,, u, m, a, c, -, 6, 4, @, o, p, e, n, s, s, h, ., c, o, m, ,, u, m, a, c, -, 1, 2, 8, @, o, p, e, n, s, s, h, ., c, o, m, ,, h, m, a, c, -, s, h, a, 2, -, 2, 5, 6, ,, h, m, a, c, -, s, h, a, 2, -, 5, 1, 2, ,, h, m, a, c, -, s, h, a, 1, ', ,,  , ', b, a, n, n, e, r,  , n, o, n, e, ', ,,  , ', f, o, r, c, e, c, o, m, m, a, n, d,  , n, o, n, e, ', ,,  , ', c, h, r, o, o, t, d, i, r, e, c, t, o, r, y,  , n, o, n, e, ', ,,  , ', t, r, u, s, t, e, d, u, s, e, r, c, a, k, e, y, s,  , n, o, n, e, ', ,,  , ', r, e, v, o, k, e, d, k, e, y, s,  , n, o, n, e, ', ,,  , ', s, e, c, u, r, i, t, y, k, e, y, p, r, o, v, i, d, e, r,  , i, n, t, e, r, n, a, l, ', ,,  , ', a, u, t, h, o, r, i, z, e, d, p, r, i, n, c, i, p, a, l, s, f, i, l, e,  , n, o, n, e, ', ,,  , ', v, e, r, s, i, o, n, a, d, d, e, n, d, u, m,  , n, o, n, e, ', ,,  , ', a, u, t, h, o, r, i, z, e, d, k, e, y, s, c, o, m, m, a, n, d,  , n, o, n, e, ', ,,  , ', a, u, t, h, o, r, i, z, e, d, k, e, y, s, c, o, m, m, a, n, d, u, s, e, r,  , n, o, n, e, ', ,,  , ', a, u, t, h, o, r, i, z, e, d, p, r, i, n, c, i, p, a, l, s, c, o, m, m, a, n, d,  , n, o, n, e, ', ,,  , ', a, u, t, h, o, r, i, z, e, d, p, r, i, n, c, i, p, a, l, s, c, o, m, m, a, n, d, u, s, e, r,  , n, o, n, e, ', ,,  , ', h, o, s, t, k, e, y, a, g, e, n, t,  , n, o, n, e, ', ,,  , ', k, e, x, a, l, g, o, r, i, t, h, m, s,  , s, n, t, r, u, p, 7, 6, 1, x, 2, 5, 5, 1, 9, -, s, h, a, 5, 1, 2, @, o, p, e, n, s, s, h, ., c, o, m, ,, c, u, r, v, e, 2, 5, 5, 1, 9, -, s, h, a, 2, 5, 6, ,, c, u, r, v, e, 2, 5, 5, 1, 9, -, s, h, a, 2, 5, 6, @, l, i, b, s, s, h, ., o, r, g, ,, e, c, d, h, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, ,, e, c, d, h, -, s, h, a, 2, -, n, i, s, t, p, 3, 8, 4, ,, e, c, d, h, -, s, h, a, 2, -, n, i, s, t, p, 5, 2, 1, ,, d, i, f, f, i, e, -, h, e, l, l, m, a, n, -, g, r, o, u, p, -, e, x, c, h, a, n, g, e, -, s, h, a, 2, 5, 6, ,, d, i, f, f, i, e, -, h, e, l, l, m, a, n, -, g, r, o, u, p, 1, 6, -, s, h, a, 5, 1, 2, ,, d, i, f, f, i, e, -, h, e, l, l, m, a, n, -, g, r, o, u, p, 1, 8, -, s, h, a, 5, 1, 2, ,, d, i, f, f, i, e, -, h, e, l, l, m, a, n, -, g, r, o, u, p, 1, 4, -, s, h, a, 2, 5, 6, ', ,,  , ', c, a, s, i, g, n, a, t, u, r, e, a, l, g, o, r, i, t, h, m, s,  , s, s, h, -, e, d, 2, 5, 5, 1, 9, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 3, 8, 4, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 5, 2, 1, ,, s, k, -, s, s, h, -, e, d, 2, 5, 5, 1, 9, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 5, 1, 2, ,, r, s, a, -, s, h, a, 2, -, 2, 5, 6, ', ,,  , ', h, o, s, t, b, a, s, e, d, a, c, c, e, p, t, e, d, a, l, g, o, r, i, t, h, m, s,  , s, s, h, -, e, d, 2, 5, 5, 1, 9, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 3, 8, 4, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 5, 2, 1, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, s, s, h, -, e, d, 2, 5, 5, 1, 9, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 5, 1, 2, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, s, h, -, e, d, 2, 5, 5, 1, 9, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 3, 8, 4, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 5, 2, 1, ,, s, k, -, s, s, h, -, e, d, 2, 5, 5, 1, 9, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 5, 1, 2, ,, r, s, a, -, s, h, a, 2, -, 2, 5, 6, ', ,,  , ', h, o, s, t, k, e, y, a, l, g, o, r, i, t, h, m, s,  , s, s, h, -, e, d, 2, 5, 5, 1, 9, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 3, 8, 4, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 5, 2, 1, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, s, s, h, -, e, d, 2, 5, 5, 1, 9, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 5, 1, 2, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, s, h, -, e, d, 2, 5, 5, 1, 9, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 3, 8, 4, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 5, 2, 1, ,, s, k, -, s, s, h, -, e, d, 2, 5, 5, 1, 9, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 5, 1, 2, ,, r, s, a, -, s, h, a, 2, -, 2, 5, 6, ', ,,  , ', p, u, b, k, e, y, a, c, c, e, p, t, e, d, a, l, g, o, r, i, t, h, m, s,  , s, s, h, -, e, d, 2, 5, 5, 1, 9, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 3, 8, 4, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 5, 2, 1, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, s, s, h, -, e, d, 2, 5, 5, 1, 9, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 5, 1, 2, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 2, 5, 6, -, c, e, r, t, -, v, 0, 1, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, s, h, -, e, d, 2, 5, 5, 1, 9, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 3, 8, 4, ,, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 5, 2, 1, ,, s, k, -, s, s, h, -, e, d, 2, 5, 5, 1, 9, @, o, p, e, n, s, s, h, ., c, o, m, ,, s, k, -, e, c, d, s, a, -, s, h, a, 2, -, n, i, s, t, p, 2, 5, 6, @, o, p, e, n, s, s, h, ., c, o, m, ,, r, s, a, -, s, h, a, 2, -, 5, 1, 2, ,, r, s, a, -, s, h, a, 2, -, 2, 5, 6, ', ,,  , ', l, o, g, l, e, v, e, l,  , v, e, r, b, o, s, e, ', ,,  , ', s, y, s, l, o, g, f, a, c, i, l, i, t, y,  , a, u, t, h, ', ,,  , ', a, u, t, h, o, r, i, z, e, d, k, e, y, s, f, i, l, e,  , ., s, s, h, /, a, u, t, h, o, r, i, z, e, d, _, k, e, y, s,  , ., s, s, h, /, a, u, t, h, o, r, i, z, e, d, _, k, e, y, s, 2, ', ,,  , ', h, o, s, t, k, e, y,  , /, e, t, c, /, s, s, h, /, s, s, h, _, h, o, s, t, _, r, s, a, _, k, e, y, ', ,,  , ', h, o, s, t, k, e, y,  , /, e, t, c, /, s, s, h, /, s, s, h, _, h, o, s, t, _, e, c, d, s, a, _, k, e, y, ', ,,  , ', h, o, s, t, k, e, y,  , /, e, t, c, /, s, s, h, /, s, s, h, _, h, o, s, t, _, e, d, 2, 5, 5, 1, 9, _, k, e, y, ', ,,  , ', a, c, c, e, p, t, e, n, v,  , l, a, n, g, ', ,,  , ', a, c, c, e, p, t, e, n, v,  , l, c, _, *, ', ,,  , ', a, u, t, h, e, n, t, i, c, a, t, i, o, n, m, e, t, h, o, d, s,  , a, n, y, ', ,,  , ', c, h, a, n, n, e, l, t, i, m, e, o, u, t,  , n, o, n, e, ', ,,  , ', s, u, b, s, y, s, t, e, m,  , s, f, t, p,  , /, u, s, r, /, l, i, b, /, o, p, e, n, s, s, h, /, s, f, t, p, -, s, e, r, v, e, r,  , ', ,,  , ', m, a, x, s, t, a, r, t, u, p, s,  , 1, 0, :, 3, 0, :, 1, 0, 0, ', ,,  , ', p, e, r, s, o, u, r, c, e, m, a, x, s, t, a, r, t, u, p, s,  , n, o, n, e, ', ,,  , ', p, e, r, s, o, u, r, c, e, n, e, t, b, l, o, c, k, s, i, z, e,  , 3, 2, :, 1, 2, 8, ', ,,  , ', p, e, r, m, i, t, t, u, n, n, e, l,  , n, o, ', ,,  , ', i, p, q, o, s,  , l, o, w, d, e, l, a, y,  , t, h, r, o, u, g, h, p, u, t, ', ,,  , ', r, e, k, e, y, l, i, m, i, t,  , 0,  , 0, ', ,,  , ', p, e, r, m, i, t, o, p, e, n,  , a, n, y, ', ,,  , ', p, e, r, m, i, t, l, i, s, t, e, n,  , a, n, y, ', ,,  , ', p, e, r, m, i, t, u, s, e, r, e, n, v, i, r, o, n, m, e, n, t,  , n, o, ', ,,  , ', p, u, b, k, e, y, a, u, t, h, o, p, t, i, o, n, s,  , n, o, n, e, ', ]
- Sysctl Settings: [, ', k, e, r, n, e, l, ., r, a, n, d, o, m, i, z, e, _, v, a, _, s, p, a, c, e,  , =,  , 2, ', ,,  , ', f, s, ., s, u, i, d, _, d, u, m, p, a, b, l, e,  , =,  , 2, ', ,,  , ', k, e, r, n, e, l, ., y, a, m, a, ., p, t, r, a, c, e, _, s, c, o, p, e,  , =,  , 1, ', ]

- UFW Status: [; '; S; t; a; t; u; s; :;  ; a; c; t; i; v; e; '; ,;  ; '; L; o; g; g; i; n; g; :;  ; o; n;  ; (; l; o; w; ); '; ,;  ; '; D; e; f; a; u; l; t; :;  ; d; e; n; y;  ; (; i; n; c; o; m; i; n; g; ); ,;  ; a; l; l; o; w;  ; (; o; u; t; g; o; i; n; g; ); ,;  ; d; i; s; a; b; l; e; d;  ; (; r; o; u; t; e; d; ); '; ,;  ; '; N; e; w;  ; p; r; o; f; i; l; e; s; :;  ; s; k; i; p; '; ,;  ; '; '; ,;  ; '; T; o;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ; A; c; t; i; o; n;  ;  ;  ;  ;  ;  ; F; r; o; m; '; ,;  ; '; -; -;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ; -; -; -; -; -; -;  ;  ;  ;  ;  ;  ; -; -; -; -; '; ,;  ; '; 2; 2; /; t; c; p;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ; A; L; L; O; W;  ; I; N;  ;  ;  ;  ; A; n; y; w; h; e; r; e;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ; '; ,;  ; '; 2; 2; /; t; c; p;  ; (; v; 6; );  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ; A; L; L; O; W;  ; I; N;  ;  ;  ;  ; A; n; y; w; h; e; r; e;  ; (; v; 6; );  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ;  ; '; ]

## Cron & At Restrictions
[
'
-
r
w
-
-
-
-
-
-
-
 
1
 
r
o
o
t
 
r
o
o
t
 
5
 
A
u
g
 
1
5
 
0
4
:
3
8
 
/
e
t
c
/
a
t
.
a
l
l
o
w
'
,
 
'
-
r
w
-
-
-
-
-
-
-
 
1
 
r
o
o
t
 
r
o
o
t
 
5
 
A
u
g
 
1
5
 
0
4
:
3
8
 
/
e
t
c
/
c
r
o
n
.
a
l
l
o
w
'
]

## /tmp Mount Options
[
]

## Time Synchronization
[
'
e
n
a
b
l
e
d
'
,
 
'
a
c
t
i
v
e
'
,
 
'
n
o
t
-
f
o
u
n
d
'
,
 
'
n
o
t
-
f
o
u
n
d
'
]

## Sudo Logging
[
'
/
e
t
c
/
s
u
d
o
e
r
s
.
d
/
1
0
-
l
o
g
f
i
l
e
:
D
e
f
a
u
l
t
s
 
l
o
g
f
i
l
e
=
/
v
a
r
/
l
o
g
/
s
u
d
o
.
l
o
g
'
,
 
'
-
r
w
-
r
-
-
-
-
-
 
1
 
r
o
o
t
 
a
d
m
 
9
9
6
5
3
 
A
u
g
 
1
6
 
0
2
:
5
4
 
/
v
a
r
/
l
o
g
/
s
u
d
o
.
l
o
g
'
]

---

## Non-Compliant Issues
No non-compliance detected.
