# MatrixOps

Matrix: A

Inverse: inv(A)

Inverse(Transpose): inv(t(A)) = t(inv(A))
(property)

Inverse(scalar matrix): inv( k*A ) = (1/k) * inv(A)

Inverse(matrix product): inv(A * B) = inv(B) %*% inv(A)

par(mar=c(3,3,1,1)+.1)
xlim <- c(-1,3)
ylim <- c(-1,3)
plot(xlim, ylim, type="n", xlab="X1", ylab="X2", asp=1)
sum <- A[1,] + A[2,]
# draw the parallelogram determined by the rows of A
polygon( rbind(c(0,0), A[1,], sum, A[2,]), col=rgb(1,0,0,.2))
vectors(A, labels=c(expression(a[1]), expression(a[2])), pos.lab=c(4,2))
vectors(sum, origin=A[1,], col="gray")
vectors(sum, origin=A[2,], col="gray")
text(mean(A[,1]), mean(A[,2]), "A", cex=1.5)
