pipeline {
    agent any 
// Добавляем триггер опроса репозитория
    triggers {
        // Проверять GitHub каждую минуту на наличие новых коммитов
        pollSCM('* * * * *')
    }
    stages {
        stage('Checkout') {
            steps {
                echo '=== Шаг 1: Код успешно скачан из GitHub ==='
            }
        }

        stage('Linter Test') {
            steps {
                echo '=== Шаг 2: Проверка качества кода ==='
                echo 'Имитируем проверку HTML и JS на ошибки (Linter)...'
            }
        }

        stage('OpenShift Prep') {
            steps {
                echo '=== Шаг 3: Подготовка к деплою в OpenShift ==='
                echo 'Формируем конфигурационный файл приложения...'
            }
        }
    }

    post {
        always {
            echo 'Пайплайн завершил работу.'
        }
    }
}
