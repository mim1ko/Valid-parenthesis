class SolutionWithoutStack {
public:
    bool isValid(string s) {
        int length = 0;

        length = s.size();
        // cout << length;
        int* array = new int[length];
        for (int i{}; i < length; i++) {
            switch (s[i]) {
            case '(':
                array[i] = 1;
                break;
            case ')':
                array[i] = -1;
                break;
            case '[':
                array[i] = 2;
                break;
            case ']':
                array[i] = -2;
                break;
            case '{':
                array[i] = 3;
                break;
            case '}':
                array[i] = -3;
                break;
            }
        }
        /*for (int t{}; t < length; t++) {
        cout << array[t] << " ";

        }*/

        // bool count_id = false;
        bool sum_id = false;
        bool correct = false;
        int sum_among = 0;
        int sum = 0;

        
            for (int i{}; i < length - 1; i++) {
                sum = sum + array[i];
                if (array[i] > 0) {
                    for (int k{i + 1}; k < length; k = k + 2) {
                        if (array[i] == -array[k]) {
                            correct = true;
                            break;
                        }else{
                            correct = false;
                        }
                    }
                } if (correct == false) {
                    return false;
                }
                for (int j{i + 1}; j < length; j = j + 2) {
                    if (array[i] == -array[j]) {
                        for (int k{i}; k <= j; k++) {
                            sum_among = sum_among + array[k];
                        }
                        if (sum_among == 0 && array[i] > array[j]) {
                            sum_id = true;
                        } else {
                            sum_id = false;
                            break;
                        }
                    }
                    sum_among = 0;
                    if (sum_id == true && (j - i) == 1) {
                        break;
                    }
                    if (sum_id == false) {
                        break;
                    }
                }
               
                
            }sum = sum + array[length-1];
        
        if (sum_id == false || sum != 0) {
            return false;
        }

        return true;
    }
};
