pipeline{
    agent any
    parameters {
        booleanParam(name: "Build", defaultValue: true)
        booleanParam(name: "Restart", defaultValue: false)
        booleanParam(name: "Shutdown", defaultValue: false)
        booleanParam(name: "Scan", defaultValue: false)
        string(name: "Branch", defaultValue: "${MOST_FREQUENT_USED_BRANCH}")
    }
    
}
