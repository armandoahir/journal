
##Rust - Log 1

##Rust basic tools

Dopo aver scaricato rust sul mio pc, ho scoperto alcuni strumenti utili che offre il programma.
C'è una funzione "cargo" che ti struttura uno scheletro di progetto rust [cargo new nomeProgetto]
E' possibile compilare con "rustc", oppure direttamente andando sul percorso dove è definito nomeProgetto1, utilizzando il tool "cargo" [cargo run nomeProgetto].
In C era mia abitudine compilare il codice soffermandomi poco sul vero significato del processo di compilazione, poco ottimizzato in caso di errori compile/runtime.
Rust ti permette di di vedere lo stato del tuo programma in modo tale da vedere eventuali errori nella fase di precompilazione, [utilizzando cargo check].
Un altro comando visto è rustfmt (rust format) che in caso di scrittura a soqquadro (cattiva indentazione, troppi spazi, etc..) ristruttura automaticamente il progetto [rustfmt nomeProgetto].

Rust is a statically and stronly typed programming language, cioè quando si definisce una variabile, le viene assegnato (se non esplicitamente) implicitamente un tipo.

fn main() {
    let x = 1;
    println!("x is {}", x);
}

il programma embedda il valore x al posto della graffa (analogia con C, dove per un intero si utilizza %d al posto delle graffe).
