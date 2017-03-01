# MATH399
\documentclass[11pt, a4paper, titlepage]{article}
\usepackage{amsmath,amsthm,amssymb}
\usepackage{enumerate}
\usepackage[all]{xy}
\begin{document}

	\date{Feb 2017}
	\title{MATH399: Riemann Surface}
	\author{Xinran Yu}
	\maketitle

	\theoremstyle{plain}
	\newtheorem{thm}{Theorem}[section]
	\newtheorem{lem}[thm]{Lemma}
	\newtheorem{coro}[thm]{Corollary}
	
	\theoremstyle{definition}
	\newtheorem{defn}[thm]{Definition}
	\newtheorem{remark}[thm]{Remark}
  
	\section{Holomorphic Function and Analytic Continuation}
	\begin{defn}[Holomorphic Function]
		Let $ D $ be an open subset of the complex plane $ \mathbb{C} $, $ f : D \to \mathbb{C} $ is a \emph{holomorphic (analytic)} function if $ f $ can be written as a power series 
		\[ f(z) = \sum_{n=0}^{\infty} (z-a)^n \frac{f^n(z)}{n\!} \]
		where $ a \in D $.
	\end{defn}
	\begin{thm}[Identity Theorem]
		If $ D $ is a connected subset of $ \mathbb{C} $ and $ f: D \to \mathbb{C} $ is a holomorphic function, with
		\[ \left. f \right|_U = 0 \]
		for some open subset $ U \subset D $, then $ f = 0 $ on $ D $.
	\end{thm}
	\begin{proof}
		Expand $ f $ as a power series about point $ a \in U $. All coefficients vanish. So $ f = 0 $ whenever power series converges.
	\end{proof}
	\textbf{ILLUSTRATION NEEDED}
	\section{Riemann surface of a holomorphic function}
	Suppose there is an open subset $ D \subset \mathbb{C} $, and a holomorphic function $ f: D \to \mathbb{C} $. 
	Fix $ z_0 \in D $, and let $ P $ be a collection of path $ \gamma: \lbrack0,1\rbrack \to \mathbb{C} $, satisfying:
	\begin{enumerate}[(i)]
		\item $ \gamma(0) = z_0 $;
		\item f can be analytically continued along $ \gamma $.
	\end{enumerate}
\textbf{ILLUSTRATION NEEDED}\\
	\begin{defn}
		An \emph{equivalence relation} $ \sim $ on $ P $, is defined by $ \gamma_0 \sim \gamma_1$ if and only if
		\begin{enumerate}
			\item[(i)] $ \gamma_0(1) = \gamma_1(1) = z_1 $, where $ z_1 \in \mathbb{C} $ is the endpoint of $ \gamma_0 $ and $ \gamma_1 $;
			\item[(ii)] $ \exists V $, an open neighbourhood of $ z_1$ such that 
			\[ \left. f_0 \right|_V = \left. f_1 \right|_V \]
			That is, analytic continuations of $ f_0 $ and $ f_1 $ along $ \gamma_0 $ and $ \gamma_1 $ respectively agree in some open 	neighbourhood of $ z_0 $.
		\end{enumerate}
	\end{defn}
	\begin{defn}
		Let $ S $ be the equivalence classes of path in $ P $, $ S:= P/\sim $, and define the \emph{quotient map} $ q $:
		\begin{align*}
			q: P &\to S\\
			\gamma &\mapsto \lbrack \gamma \rbrack_\sim
		\end{align*}
	\end{defn}
	\begin{defn}
		A subset $ U \subset S $ is \emph{open}, if and only if $ q^{-1}(U) \subset P $ is open.
	\end{defn}
	Then there are maps
	\[\begin{matrix}
		\xymatrix{
			P \ar@/_/[ddr]_{ \gamma \mapsto \gamma \lbrace 1 \rbrace } \ar[dr]^q\\			
			&S \ar[d]^{\pi} \ar[r]^{ \tilde{f} } & \mathbb{C} \\
			& \mathbb{C}
		}
	\end{matrix}\]
	where 
	\[ \pi(\lbrack \gamma \rbrack) = \gamma(1) \] 
	and
	\[ \tilde{f}(\lbrack \gamma \rbrack) = f_\gamma (\gamma(1)) \]
	
	\begin{remark}\
		\begin{enumerate}
			\item[(i)] $ \pi q (\gamma) = \gamma(1) $. The function is continuous because $ \forall $ open subset $ U \subset \mathbb{C} $,
			\[ P_{ \lbrace1\rbrace, U }= \lbrace \gamma \in P \mid \gamma(1) \in U \rbrace \subset P \]
			and the left hand side is exactly $ (\pi q)^{-1}(U)$;
			\item[(ii)] it follows that $ \pi $ is also a continuous function: $ \forall $ open subset $ U \subset \mathbb{C} $, $ (\pi q)^{-1}(U) = q^{-1} ( \pi^{-1}(U)) $ is open in $ P $. By the definition of open subsets in $ S $, $ \pi^{-1}(U) $ is open.
		\end{enumerate}
	\end{remark}
\end{document}
