# Draft3 -- \today 


## Conjecture: The two assumptions below are satisfied by all elementary functions on $\mathbb{R}$

* (a) The domain of $f$ is the union of an `effective exhaustion` 
* (b) $f$ is `effectively locally uniformly continuous` w.r.t. this exhaustion 

In order to prove that the above conditions hold for elementary functions, 
first we will strengthen the first condition and prove that the resullting two conditions below are satisfied by elementary functions:

* (c) Having an open set $U$ with an effective open exhaustion, $f^{-1}(U)$ is either the empty set or has an effective open exhaustion.
* (d) for non-empty $f^{-1}(U)$, $f$ is effectively locally uniformly continuous w.r.t. this exhaustion 

Then, since $\mathbb{R}$ has an open exhaustion, and we know that for every function on $\mathbb{R}$, the domain of $f$ can be written as $f^{-1}(\mathbb{R})$, we can easily see that the conditions (a) and (b) themselves hold for all elementary functions.

\color{purple}
## Elementary functions definition:


\color{black}
An equivalent definition of elementary functions on $\mathbb{R}$ is given in \color{blue} [here](https://muleshko.faculty.unlv.edu/handouts/Elementary%20Functions%20(1).pdf).

\color{black}
#### Definition 1.
The following eight functions are referred to as the *fundamental elementary functions* of a real variable,

* $f_1(x) = c$,  $c \in \mathbb{R}$ with domain $D \subseteq \mathbb{R}$

* $f_2(x) = x$ with domain $D \subseteq \mathbb{R}$

* $f_3(x) = \frac{1}{x}$ with domain $D \subseteq \mathbb{R} \setminus \{ 0 \}$

* $f_4(x) = \sqrt[n]{x} , n \in \mathbb{N}$ if $\frac{n}{2} \in \mathbb{N}$ then domain $D \subseteq [0, +\infty )$ and  if $\frac{n+1}{2} \in \mathbb{N}$ then domain $D \subseteq \mathbb{R}$

* $f_5(x) = \sin{x}$ with domain $D \subseteq \mathbb{R}$

* $f_6(x) = e^x$ with domain $D \subseteq \mathbb{R}$

* $f_7(x) = \ln{x}$ with domain $D \subseteq (0, +\infty )$

* $f_8(x) = \arccos{x}$ with domain $D \subseteq [-1,1]$

#### Definition 2.
For any two functions (of a real variable) $f(x)$ and $g(x)$ with
domains $D_f$ , $D_g$ and ranges $R_f$ , $R_g$, respectively, the following operations are called The *Fundamental Elementary Operations* on Functions:

* Addition, Multiplication, and

* Composition of Functions

\color{teal}
### We prove the conditions (c) and (d) for elementary functions by induction on the structure of the functions.

\color{black}
#### Induction Base : The two assumptions (c) and (d) hold for fundamental elementary functions of a real variable, i.e $f_1, f_2, ... , f_8$

* Proof for $f_1(x) = c$:

    1. Claim (c) : ${f_1}^{-1}(U)$ is either the empty set or has an effective open exhaustion.

        There willl be two cases:

        1. $c\in U$. Which makes ${f_1}^{-1}(U) = \mathbb{R}$.
            In this case, the effective open exhaustion 
            $(U_l) = (U_1, U_2, ..., U_n, ...)$ where $U_i$ is the interval
            $(-i, i)$ is an effective exhaustion for $\mathbb{R}$. 

        2. $c\notin U$. Which makes ${f_1}^{-1}(U) = \emptyset$

    2. Claim (d) : for non-empty ${f_1}^{-1}(U)$, $f$ is effectively locally uniformly continuous w.r.t. the exhaustion $(U_l)$.

        We would have to provide the recursive function
        $M:\mathbb{N}^2 \mapsto \mathbb{N}$ such that for all $k,l$ and all $x,y \in U_l \\$
        $$(*)\quad |x-y| < 2^{-M(k,l)} \quad \Rightarrow |f_1(x) - f_1(y)| < 2^{-k}.\\$$
        Putting $M(k,l) := 0$, since $f$ is the constant function, we will have the implication (*) above.

* Proof for $f_2(x) = x$:

    1. Claim (c) : ${f_2}^{-1}(U)$ is either the empty set or has an effective open exhaustion.

        Since $f_2^{-1}(U) = U$, $(U_l)$ is also an open effective exhaustion for $f_2^{-1}(U)$.

    
    2. Claim (d) : for non-empty ${f_1}^{-1}(U)$, $f$ is effectively locally uniformly continuous w.r.t. the exhaustion $(U_l)$.

        We would have to provide the recursive function $M:\mathbb{N}^2 \mapsto \mathbb{N}$ such that for all $k,l$ and all $x,y \in U_l \\$
        $$(*)\quad |x-y| < 2^{-M(k,l)} \quad \Rightarrow |f_2(x) - f_2(y)| < 2^{-k}.\\$$

        Putting $M(k,l) := k$, turns the above implication into a tautology.

* Proof for $f_3(x) = \frac{1}{x}$:

    1. Claim (c) : ${f_3}^{-1}(U)$ is either the empty set or has an effective open exhaustion.
        
        Since no element can be mapped to $\{ 0 \}$ using $f_3$, we consider the open exhaustion $(U'_l)$ constructed by \textbf{Lemma 4} for $U \setminus \{ 0 \}$.
        
        Now looking at each arbitrary stage $U'_k$, we get finitely many intervals $(a^m_1, b^m_1), (a^m_2, b^m_2), ..., (a^m_{r-1}, b^m_{r-1}), (a^m_{r},b^m_{r}), .... , (a^m_{m_k},b^m_{m_k})$. where the start and endpoint of each interval is non-zero and in $\mathbb{Q}$ (by definition of effective exhaustion).

        By the construction, none of these intervals contain 0, so let's assume $(a^m_{r},b^m_{r})$ is the first interval with positive values.

        Let's define $U''_m = ((\frac{1}{b^m_{r-1}}, \frac{1}{a^m_{r-1}}) , ... ,(\frac{1}{b^m_{1}}, \frac{1}{a^m_{1}}), (\frac{1}{b^m_{m_k-1}}, \frac{1}{a^m_{m_k-1}}), ... , (\frac{1}{b^m_r}, \frac{1}{a^m_r}))$

        Claim: $(U''_m)$  is an effective open exhaustion for $f_3^{-1}(U) = f_3^{-1}(U\setminus \{ 0 \})$.
        \color{red}
        TODO
        \color{black}
    
    2. Claim (d) : for non-empty ${f_1}^{-1}(U)$, $f$ is effectively locally uniformly continuous w.r.t. the exhaustion $(U''_M)$.

        We would have to provide the recursive function $M:\mathbb{N}^2 \mapsto \mathbb{N}$ such that for all $k,l$ and all $x,y \in U''_M \\$
        $$(*)\quad |x-y| < 2^{-M(k,l)} \quad \Rightarrow |\frac{1}{x} - \frac{1}{y}| = |\frac{y - x}{xy}| < 2^{-k}.\\$$

        We need to define $M(k,l)$ in a way that forall $x,y \in U_l$ $2^{-M(k,l)} < 2^{-k} |xy|$. Now let's define $s(l) := |min(a_1, b_{m_k-1})|$. Then we'll have to define  $M(k,l)$ in a way that $2^{-M(k,l)} < 2^{-k} |s(l)^2|\\$
        $$\quad 2^{-M(k,l)} < 2^{-k} |s(l)^2|\\$$
        $$\Leftrightarrow 2^{k-M(k,l)} <|s(l)^2|\\$$
        $$\Leftrightarrow k-M(k,l) < \log _2(s(l)^2)$$
        $$\Leftrightarrow k - \log _2(s(l)^2) <  M(k,l)\\$$  
        So defining $M(k,l) := \lceil k - \log _2(s(l)^2) \rceil$ would satisfy (*).

---

* Proof for $f_4(x) = \sqrt[n]{x} , n \in \mathbb{N}$:


    For the case where $\frac{n}{2}\in \mathbb{N}$:

    We need to totalize the function $f_4(x)$ for even $n$ -- We define $f_4(x)$ to be 0 when $x<0$.

    1. Claim (c) : ${f_4}^{-1}(U)$ is either the empty set or has an effective open exhaustion.


        ${f_4}^{-1}(U) = \{ x | \sqrt[n]{x}\in U \} = \{ x^n | x\in U \}$
        
        Let's look at the union of intervals $U_l$.

        Since the open exhaustion is effective, let's iterate on intervals and construct $U'_l$s respectively. For all intervals with both ends in negative numbers,(since no value is mapped to negative numbers) the intervals will be ignored and no interval will be added.

        Since the closure of intervals in the original open set $U_l$ are disjoint, there will be at most one interval $I^l_j = (a^l_j, b^l_j)$ with $0 \in I^l_j$. In this case, since the $0$ is included in $U$, we will have to union $(-l,  {b^l_j}^n )$ with the already constructed $U'_i$.
        Note that by property (3) of open exhaustions if $\exists k \in \mathbb{N} \quad s.t. \quad 0 \in U_k$ then $\forall k'>k \quad 0 \in U_{k'}$. This means that the construction we are using, guarantees that $(U'_l)$ will be  covering all negative numbers in case $0 \in U$.

        For the intervals $I^l_j = (a^l_j, b^l_j)$ with both ends in positive numbers,  we will only need to scale; i.e we have to union $({a^l_j}^n,  {b^l_j}^n )$ with the already constructed $U'_i$.

        \color{red}
        TODO prove the construction actually gives us an open exhaustion. [clear, yet needs to be proved]
        \color{black}

    2. Claim (d) : for non-empty ${f_4}^{-1}(U)$, $f$ is effectively locally uniformly continuous w.r.t. the exhaustion $(U''_M)$.

        We would have to provide the recursive function $M:\mathbb{N}^2 \mapsto \mathbb{N}$ such that for all $k,l$ and all $x,y \in U''_M \\$
        $$(*)\quad |x-y| < 2^{-M(k,l)} \quad \Rightarrow |\sqrt[n]{x} - \sqrt[n]{y}| < 2^{-k}.\\$$

        \color{red}
        TODO
        \color{black}

    For the case where $\frac{n+1}{2}\in \mathbb{N}$:

    1. Claim (c) : ${f_4}^{-1}(U)$ is either the empty set or has an effective open exhaustion.

        ${f_4}^{-1}(U) = \{ x  | \sqrt[n]{x}\in U \} = \{ x^n | x\in U \}$$

        Let's construct $(U'_l)$ from the open exhaustion $(U_l)$ of $U$. Looking at $U_l = ((a^l_1, b^l_1), (a^l_2, b^l_2), ..., (a^l_{k_l}, b^l_{k_l}) )$, the corresponding stage in $U'_l$ would be $(({a^l_1}^n, {b^l_1}^n), ({a^l_2}^n, {b^l_2}^n), ..., ({a^l_{k_l}}^n, {b^l_{k_l}}^n) )$ 
        \color{red} TODO prove this is an effective open exhaustion
        \color{black}


    2. Claim (d) : for non-empty ${f_4}^{-1}(U)$, $f$ is effectively locally uniformly continuous w.r.t. the exhaustion $(U'_l)$.

        We would have to provide the recursive function $M:\mathbb{N}^2 \mapsto \mathbb{N}$ such that for all $k,l$ and all $x,y \in U''_M \\$
        $$(*)\quad |x-y| < 2^{-M(k,l)} \quad \Rightarrow |\sqrt[n]{x} - \sqrt[n]{y}| < 2^{-k}.\\$$

        \color{red} 
        TODO
        \color{black}


* Proof for $f_5(x) = \sin{x}$:

    1. Claim (c) : ${f_5}^{-1}(U)$ is either the empty set or has an effective open exhaustion.

        ${f_5}^{-1}(U) = \{ x  | \sin{x}\in U \} = \{ \cup_{i=1}^\infty (2i\pi + x) | \sin{x}\in U \}$
        If $[-1,1] \cup U = \emptyset$, then ${f_5}^{-1}(U) = \emptyset$. Now let's assume $[-1,1] \cup U \neq \emptyset$ 

        \color{red} 
        TODO
        \color{black}

    2. Claim (d) : for non-empty ${f_1}^{-1}(U)$, $f$ is effectively locally uniformly continuous w.r.t. the exhaustion $(U'_l)$.

        We would have to provide the recursive function $M:\mathbb{N}^2 \mapsto \mathbb{N}$ such that for all $k,l$ and all $x,y \in U''_M \\$
        $$(*)\quad |x-y| < 2^{-M(k,l)} \quad \Rightarrow |\sqrt[n]{x} - \sqrt[n]{y}| < 2^{-k}.\\$$



* Proof for $f_6(x) = e^x$:

* Proof for $f_7(x) = \ln{x}$:

* Proof for $f_8(x) = \arccos{x}$:



#### Induction Step : If the two assumptions hold for $f,g$, then they will also hold for
#####  (1) Addition($(f+g)(x)$)
#####  (2) Multiplication($(f.g)(x)$) and
#####  (3) Composition($f\circ g(x)$)

<!-- 
* Proof: Cases of addition and multiplication are similar since 
    $D_{f+g(x)} = D_f \cap D_g = D_{f.g(x)}$. Proof by \color{cyan} \textbf{Lemma 1}.
    \color{black}

* Proof for function composition:
    
    * Let's denote the effective exhaustions for domains of $f$, $g$, and   $f\circ g$ respectively by $U = (U_1, U_2, ...)$, $U' = (U_1, U_2, ... )$, and $U'' = (U''_1, U''_2, ...)$.
    * Using \color{violet} \textbf{Lemma 3} \color{black}, $g^{-1}(D_f)$
    has an open exhaustion. 

    * Now we'll have to prove that $f\circ g$ is effectively locally uniformly continuous w.r.t. that exhaustion. Proof by \color{orange} \textbf{Lemma 2}.
    \color{black}

---


\color{orange}
##### Lemma 2:

Let $f, g$ be two functions on $\mathbb{R}$ and $D_f$ and $D_g$ be the domains covered by effective open exhaustions $U_f, U_g$ such that the domains are effectively locally uniformly continuous w.r.t $D_f$ and $D_g$ respectively. Then $f\circ g$ is effectively locally uniformly continuous w.r.t an open exhaustion (below) on $g^{-1}(D_f)$.

\color{black}

##### Proof of Lemma 2:


In order to prove effective local uniform continuity w.r.t $D_{{f\circ g}_l}$, we would have to show there is a recursive function $M:\mathbb{N}^2 \mapsto \mathbb{N}$ such that for all $k,l$ and all $x,y \in D_{{f\circ g}_l}\\$
$|x-y| < 2^{-M(k,l)} \quad \Rightarrow |f(x) - f(y)| < 2^{-k}.\\$
Let's take arbitrary $k, l$.

---

\color{violet}
##### Lemma 3:

Let $g$ be effectively locally uniformly continuous on its domain w.r.t. exhaustion $(U^D_l)$ of the domain and let $U$ be an open set with the sequences $(U_1, U_2, ...)$ being the effective open exhaustions (where each $U_l^k$ consists of finitely many intervals $I_1^l, I_2^l, ... , I_{k_l}^l$) ; Then $g^{-1}(U)$ would have an effective open exhaustion. 

\color{black}
##### Proof of Lemma 3:


* Claim 3-1 : The sequence of open sets $U' = (g^{-1}(U_1), g^{-1}(U_2), ...)$ is an effective open exhaustion for $g^{-1}(U)$

Claim 3-1 can be broken into the two following claims:

* Claim 3-2:
    $U' = (g^{-1}(U_0), g^{-1}(U_1), ...)$  is an open exhaustion.

    proof: We need to prove the following 3 properties:

    * $g^{-1}(U) = \bigcup^{\infty}_{l=1} g^{-1}(U_l)\\$

        proof:

        $\quad x \in g^{-1}(U)\\$
        $\Leftrightarrow \exists y \in U \quad y = g(x)\\$
        $\Leftrightarrow \exists y \in \bigcup_{l=1}^{\infty} U_l \quad y = g(x) \quad$ since $(U_l)$ is an open exhaustion for $U\\$
        $\Leftrightarrow \exists k \in \mathbb{N} \quad \exists y \in U_k \quad y = g(x) \\$
        $\Leftrightarrow \exists k \in \mathbb{N} \quad x \in g^{-1}(U_k) \\$
        $\Leftrightarrow x \in \bigcup_{l=1}^{\infty} g^{-1}(U_l) \\$
        

    
    * For $l \in \mathbb{N}$, $g^{-1}(U_l)$ is a *finite* union of non-empty finite open intervals $I'^l_i \quad i = 1, ..., k_l$ whose closures are pairwise *disjoint*.

        proof:

        Let's define $I'^l_i := g^{-1}(I_i^l)$. all $k_l$s are finite by definition. It only remains to show that (1) $I'^l_i$ are finite open intervals and (2)  $\overline{I'^l_i}$s are disjoint

        * proof of (1):
        
            For $I_i^l$, let's take the center of the interval $c_i^l$ and call the length of the interval $d_i^l$, Now let's use the "effective local uniform continuity" property of $g$.

            There is a recursive function $M:\mathbb{N}^2 \mapsto \mathbb{N}$ such that for all $k,l$ and all $x,y \in U^D_l \\$
            $|x-y| < 2^{-M(k,l)} \quad \Rightarrow |g(x) - g(y)| < 2^{-k}.\\$

            Putting $l := l$ and choosing $k$ big enough such that $2^{-k} = d_i^l$, it gives us a recursively computable bound $2^{-M(k,l)}$ such that 

        * proof of (2):



    * $\overline{g^{-1}(U_l)} = \bigcup^{\infty}_{i=1} \overline{I_i^l} \subseteq g^{-1}(U_{1+1})$ for $l=1,2, ...$

* Claim 3-3:
    $U' = (g^{-1}(U_1), g^{-1}(U_2), ...)$ is an *effective* open exhaustion.


---

 -->


#### Lemma 1:


Let $U, U'$ be open sets with $U \cap U' \neq \emptyset$ and the sequences $(U_l) = (U_1, U_2, ...), (U'_l) = (U'_1, U'_2, ...)$ be effective open exhaustions for $U, U'$ (respectively). The open exhaustion $U''$ defined below is an effective open exhaustion of $U \cap U'$.

\color{black}
##### Proof of Lemma 1:

 
* Claim 1-1 : There exists $k \in \mathbb{N}$ s.t $U_k \cap U'_k \neq \emptyset$.

    We know that $U \cap U' \neq \emptyset \\$
    $\Rightarrow \exists m \in U \cap U' \\
    \Rightarrow \exists m \quad m \in U \land m \in U'\\
    \Rightarrow \exists m \quad m \in \bigcup_{l=0}^\infty U_l \land m \in \bigcup_{l=0}^\infty U'_l \\
    \Rightarrow \exists m \quad \exists l_m, l'_m \in \mathbb{N} \quad m \in U_{l_m} \land m \in U'_{l'_m} \quad\\$ 
    Putting $k = max \{ l_m, l'_m \}$,
    since we have the property(3) of exhaustion for both $U$ (and respectively $U'$), i.e. $\forall l\in \mathbb{N} \quad U_l \subseteq \overline{U_l} \subseteq U_{l+1}\\$
    $\Rightarrow \exists m \quad \exists k \in \mathbb{N} \quad m \in U_k \land m \in U'_k\\$
    $\Rightarrow \exists m \quad \exists k \in \mathbb{N} \quad m \in U_k \cap U'_k\\$
    $\Rightarrow \exists k \in \mathbb{N} \quad U_k \cap U'_k \neq \emptyset$
    
* Note: $\bigcup_{l=1}^{\infty} U_l = \bigcup_{l=k}^{\infty}$

* Claim 1-2 : The sequence $U'' = (U_k \cap U'_k, U_{k+1} \cap U'_{k+1}, ...)$ is an effective open exhaustion for $U \cap U'$

    1.  Proof for property (1) of the definition of open exhaustion: i.e $U \cap U' = \bigcup_{l = k}^\infty (U''_l).\\$Starting at the LHS:$\\$
    $x\in U \cap U'\\$
    $\Leftrightarrow x \in \bigcup_{l=1}^\infty U_l \quad \land \quad x \in \bigcup_{l'=1}^\infty U_l'\\$
    $\Leftrightarrow \exists l,l'>0 \quad x\in U_l \quad \land \quad x\in U'_{l'}\\$
    Putting $l_{max} := max \{ l, l' \}$ and by property (3) of $(U_l), (U'_{l'}):\\$
    $\Leftrightarrow \exists l_{max}>0 \quad x\in U_{l_{max}} \quad \land \quad x\in U'_{l_{max}}\\$
    $\Leftrightarrow \exists l_{max}>0 \quad x\in U_{l_{max}} \cap U'_{l_{max}}\\$
    $\Leftrightarrow x\in \bigcup_{l = 1}^\infty (U_l \cap U'_l)\\$
    $\Leftrightarrow x\in \bigcup_{l = k}^\infty (U_l \cap U'_l )\\$
    $\Leftrightarrow x\in \bigcup_{l = k}^\infty (U''_l)\\$
    
    2. Proof for property (2) of the definition of open exhaustion: For $l \in \mathbb{N}$, $(U'_l)$ is a *finite* union of non-empty finite open intervals $I'^l_i \quad i = 1, ..., k_l$ whose closures are pairwise *disjoint*.

    \color{red}
    TODO
    \color{black}

    3. Property (3) of the definition of open exhaustion: 
    $\\ \overline{g^{-1}(U_l)} = \bigcup^{\infty}_{i=1} \overline{I_i^l} \subseteq g^{-1}(U_{1+1})$ for $l=1,2, ...$

    Clear by construction. (miiight need some explanation)

    4. $U' = (g^{-1}(U_1), g^{-1}(U_2), ...)$ is an *effective* open exhaustion.
    
    Clear by construction. (miiight need some explanation)


    


##### Lemma 4:
If $(U_l)$ is an effective open exhaustion for the open set $U$, then for any single point $r \in \mathbb{R}$ there is an open exhaustion for $U \setminus \{ r \}$ .

\color{black}

Proof:

\color{red}
TODO : check to see if $U_l$s are non-empty
\color{black}

Let's show he sequence $(U'_l)$ with $U'_i = U_i \setminus [r - \frac{1}{i}, r + \frac{1}{i}]$ is an open exhaustion for $U' = U \setminus \{ r \}$.


1.  Proof for property (1) of the definition of open exhaustion: $U' = \bigcup_{l = 1}^\infty U'_l:\\$
    $x\in U'\\$
    $\Leftrightarrow x \in U \land x \neq r\\$
    $\Leftrightarrow x \in \bigcup_{l = 1}^\infty U_l \land x \neq r\\$
    $\Leftrightarrow \exists k \in \mathbb{N} \quad x \in U_k \land x \neq r\\$
    $\Leftrightarrow \exists k \in \mathbb{N} \quad \exists \epsilon \neq 0 \quad  x = r + \epsilon \in U_k\\$
    (Selecting $k' :=$the smallest value such that $k' = k$ and $|\epsilon| > \frac{1}{k'}$, knowing property 3 of exuahstion holds for $(U_l)$)

    $\Leftrightarrow \exists k'\in \mathbb{N} \quad \exists \epsilon \neq 0 \quad |\epsilon| > \frac{1}{k'} \quad  \land \quad  x = r + \epsilon \in U_{k'}\\$
    $\Leftrightarrow \exists k' \quad \exists \epsilon \neq 0 \quad  x = r + \epsilon \in U_{k'} \quad \land \quad r + |\epsilon| > r + |\frac{1}{k'}|\\$
    $\Leftrightarrow \exists k' \quad  x \in U_{k'} \quad \land \quad x\notin [r - \frac{1}{k'}, r + \frac{1}{k'}]\\$
    $\Leftrightarrow \exists k' \quad  x \in U_{k'} \setminus [r - \frac{1}{k'}, r + \frac{1}{k'}]\\$
    $x \in \bigcup_{l = 1}^\infty U'_l$

2. Proof for property (2) of the definition of open exhaustion: For $l \in \mathbb{N}$, $(U'_l)$ is a *finite* union of non-empty finite open intervals $I'^l_i \quad i = 1, ..., k_l$ whose closures are pairwise *disjoint*.

    Since we are only modifying a previously-existing open exhaustion $(U_l)$ by removing points from it, $U'_l$ is still going to be consisting of disjoint sets.
    
    Now we need to prove that $U'_l$ consists only of finitely many "open intervals". Note that we are beginning with a set of open intervals on $\mathbb{R}$ and subtracting a single closed interval(which is the same as taking the intersection with two open intervals) which in turn gives us finitely many open intervals.

3. Property (3) of the definition of open exhaustion: $\overline{g^{-1}(U_l)} = \bigcup^{\infty}_{i=1} \overline{I_i^l} \subseteq g^{-1}(U_{1+1})$ for $l=1,2, ...$

    Clear by construction. (miiight need some explanation)

4. $U' = (g^{-1}(U_1), g^{-1}(U_2), ...)$ is an *effective* open exhaustion.
    
    Clear by construction. (miiight need some explanation)

---