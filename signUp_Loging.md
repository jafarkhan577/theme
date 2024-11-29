function signupUser() {
    const email = document.getElementById("signupEmail").value;
    const password = document.getElementById("signupPassword").value;
    
    auth.createUserWithEmailAndPassword(email, password)
        .then((userCredential) => {
            alert("Signup successful!");
        })
        .catch((error) => {
            alert(error.message);
        });
}
function loginUser() {
    const email = document.getElementById("loginEmail").value;
    const password = document.getElementById("loginPassword").value;
    
    auth.signInWithEmailAndPassword(email, password)
        .then((userCredential) => {
            alert("Welcome back!");
        })
        .catch((error) => {
            alert("Invalid credentials.");
        });
}
