# rust
pub fn plus_one(mut digits: Vec<i32>) -> Vec<i32> {
    let mut carry = 1;
    for i in (0..digits.len()).rev() {
        let sum = digits[i] + carry;
        digits[i] = sum % 10;
        carry = sum / 10;
    }
    if carry > 0 {
        digits.insert(0, carry);
    }
    digits
}
