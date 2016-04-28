# [](#falafel)falafel

Wrapping a function:

    function walk (node) {
      if (node.type === 'FunctionDeclaration') {
        if (node.id.name === 'findWord') {
          const orig = node.source.toString()
          node.body.update('{ return 99 }')
        }
      }
    }
