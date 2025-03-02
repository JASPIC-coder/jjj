# jjj 
A) function countMembershipLevels(members) {
    const count = {};
    members.forEach(member => {
        if (member.membership) {
            count[member.membership] = (count[member.membership] || 0) + 1;
        }
    });
    return count;
}

B) function getGoldMembers(members) {
    return members.filter(member => member.membership === "gold").map(member => member.name);
}

C)  function getGoldMembersSafe(members) {
    if (!Array.isArray(members) || members.length === 0) return "No gold members found";

    const goldMembers = members
        .filter(member => member.membership === "gold")
        .map(member => member.name);

    return goldMembers.length > 0 ? goldMembers : "No gold members found";
}

D)  function generateWelcomeMessages(members) {
    return members.map(member => `Welcome, ${member.name}! You are a ${member.membership} member.`);
}

E) Map is preferred over tradtional loop  because:
  by performance; map is generally fasterwhen the operation being applied to the array is is simple as it is optimizesthe transformation internally
  by readability;using map make codesmore concise, easier to understand and reduce the risks of errors
   
